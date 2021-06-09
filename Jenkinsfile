pipeline {
    agent any
    stages {
        stage('build') {
            steps {
               
                gcloud compute instances create third  {"image-family":centos-7, "image-project":centos-cloud", "zone":europe-west2-c}
            }
        }
    }
}
