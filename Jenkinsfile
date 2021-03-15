pipeline {
    agent any
    stages {
         withKubeConfig([credentialsId: 'kubecrt4']) {
          stage("Apply Kubernetes filest") {
           
            steps{
                sh "kubectl apply -f deploy.yml"
            }
           }                      
       }
    }
}
