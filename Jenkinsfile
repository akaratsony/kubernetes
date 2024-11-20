pipeline {
    agent any
    stages {
        stage('Create Replicaset using the configured yaml file. ') {
            steps {
                script {
                    sh 'git pull "sudo git clone https://github.com/akaratsony/kubernetes.git"'
                    sh 'sudo kubectl create -f replicaset.yaml'
                    sh 'kubectl get replicaset'
                    sh 'kubectl get pods'
                }
            }
        }
        stage('Create Deployment using the configured yaml file. ') {
            steps {
                script {
                    sh 'git pull "sudo git clone https://github.com/akaratsony/kubernetes.git"'
                    sh 'sudo kubectl create -f deployment.yaml'
                    sh 'kubectl create -f deployment.yaml'
                    sh 'kubectl get deployments'
                    sh 'kubectl get pods'
                    sh 'kubectl describe deployment myapp-deployment'
                    sh 'kubectl get all'
                }
            }
        }
        stage('Create service using the configured yaml file. ') {
            steps {
                script {
                    sh 'git pull "sudo git clone https://github.com/akaratsony/kubernetes.git"'
                    sh 'sudo kubectl create -f service-definition.yaml'
                    sh 'kubectl get svc'
                }
            }
        }
      
    }
}
