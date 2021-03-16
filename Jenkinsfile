pipeline {
    agent any
    stages {
          stage("Apply Kubernetes filest") {
           
            steps{
                sh "kubectl apply -f deploy.yml"
            }
       }
    }
}
