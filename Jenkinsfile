pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                
              account='poras08@uplifted-plate-316209.iam.gserviceaccount.com'
              path='C:\Users\poras\Downloads\uplifted-plate-316209-17f20e00a10c.json'
              gcloud compute instances create third  --image-family=centos-7 --image-project=centos-cloud --service-account=$account --metadata-from-file=$path
            }
        }
    }
}
