pipeline{
  agent any
  stages {

     stage('Build'){
        steps {
             sh 'python --version'
             echo "Hello World"
             bat label:'', script: 'python main.py'

        }
     }
  }
}