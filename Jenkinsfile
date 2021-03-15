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
       stage("Apply Kubernetes files") {
       withKubeConfig([credentialsId: 'kubecrt4']) {
       sh "kubectl apply -f deploy.yml"
                }
           }

    }
}
