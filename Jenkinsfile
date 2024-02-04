pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''./mvnm sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://65.0.56.175:9000 \\
  -Dsonar.token=sqp_3482ff6ce36a4f73eb4e756b412245930a99a34b'''
      }
    }

  }
}