pipeline {
    agent any
    stages {
          stage("Apply Kubernetes filest") {
            withKubeConfig([credentialsId: 'kubecrt4']) {
            steps{
                sh "kubectl apply -f deploy.yml"
            }
           }                      
       }
    }
}
