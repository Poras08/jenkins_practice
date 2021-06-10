pipeline {
    agent any
    stages {
        
        stage ('Checkout'){
            steps {checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'c0b259b2-ae10-4a42-8f86-16c1285b3472', url: 'https://github.com/Poras08/jenkins_practice.git']]])
                  }
            
        }
        stage('build') {
            steps {
               git credentialsId: 'c0b259b2-ae10-4a42-8f86-16c1285b3472', url: 'https://github.com/Poras08/jenkins_practice.git'
               sh 'python main.py'
            }
        }
    }
}
