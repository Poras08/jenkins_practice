pipeline {
    agent {
        docker {
             
             image 'gcr.io/google.com/cloudsdktool/cloud-sdk:latest'
        }
    
    }
    stages {
        
        stage ('Checkout'){
            steps {checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'c0b259b2-ae10-4a42-8f86-16c1285b3472', url: 'https://github.com/Poras08/jenkins_practice.git']]])
                  }
            
        }
        stage('Show') {
            steps {
                  sh label:"List all images",
                     script: """
                             Path = "$WORKSPACE/key.json"
                             gcloud auth activate-service-account poras08@uplifted-plate-316209.iam.gserviceaccount.com  --key-file=${Path} --project=MY First Project
                             gcloud compute instances create fourth --image-family=centos-7 --image-project=centos-cloud --zone=europe-west2-c
                             """      
            }
        }
    }
}
