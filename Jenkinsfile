library identifier: 'jenkins-shared-lib-demo1@master',
        retriever: modernSCM([$class: 'GitSCMSource',
         remote: 'https://github.com/hhammidd/jenkins-shared-lib-demo1.git'])

properties([
  parameters([
    string(name: 'IMAGE_TAG', defaultValue: '11', description: 'Image TAG', )
   ])
])

pipeline {
    environment {
        registry = "hhssaaffii/docker-jenkins"
        registryCredential = ''
        dockerImage = ''
    }
    agent any
    stages {
        stage("test shared") {
                steps{
                    doEcho()
                }
            }

        stage("git checkout") {
            steps{
                git 'https://github.com/hhammidd/app-jenkins.git'
            }
        }

        stage("build-test") {
            steps{
                sh "mvn clean install"
            }
        }
        stage("build Image") {
            steps{
                script {
                    dockerImage = docker.build registry + ":$BUILD_NUMBER"
                }
            }
        }
             

       
        stage("Install helm and deploy") {
            steps{
                sh " helm upgrade docker-jenkins  ingress/helm-demo1 --set tag=${params.IMAGE_TAG}"
            }
        }

    }
}
