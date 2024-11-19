pipeline {
    agent any
    stages {
        stage('Create Replicaset using the configured yaml file. ') {
            steps {
                script {
                    // Installation of docker for CentOS
                    sh 'git pull "sudo git clone https://github.com/akaratsony/kubernetes.git"'
                    sh 'sudo kubectl create -f replicaset.yaml'
                    sh 'kubectl get replicaset'
                    sh 'kubectl get pods'
                  //test the failover -> kubectl delete pod my-app-replicaset-8nxxl
                }
            }
        }
      
    }
}
