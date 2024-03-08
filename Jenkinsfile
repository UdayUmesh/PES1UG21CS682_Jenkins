pipeline{
  agent any
  stages {
    stage('Build') {
        steps {
          build 'PES1UG21CS682-1'
          sh 'g++ main.cp -o output'
        }
    }
    stage('Test') {
       steps {
         sh './output'
       }
    }
    stage('Deploy') {
       steps {
           echo 'deploy'
       }
    }
  }
    post{
      failure{
        error 'Pipeline failed'
      }
    }
}
