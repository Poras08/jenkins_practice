pipeline {
    agent any
    stages {
        
        stage ('Checkout'){
            steps {checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'c0b259b2-ae10-4a42-8f86-16c1285b3472', url: 'https://github.com/Poras08/jenkins_practice.git']]])
                  }
            
        }
        stage('Show') {
            steps {
                  sh label:"List all images",
                     script: """
                             gcloud compute instances create centos5 --image-family=centos-7 --image-project=centos-cloud
                             """      
            }
        }
    }
}
