pipeline {
    agent any
    stages {
        stage('build') {
            steps {
              gcloud compute instances create third  --image-family=centos-7 --image-project=centos-cloud --service-account=poras08@uplifted-plate-316209.iam.gserviceaccount.com
            }
        }
    }
}
