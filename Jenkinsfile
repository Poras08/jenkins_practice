pipeline{
  agent any
  stages {
    
    stage('Create'){
      steps {
             gcloud compute instances create new-instance  --image-family=centos-7 --image-project=centos-cloud  --zone=europe-west2-c 
      
      }
    
    }

     
  }
}
