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
        sh '''./mvn sonar:sonar \\
  -Dsonar.host.url=http://65.0.56.175:9000 \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.token=sqp_f12c2298d77b7916325eff3c2ad42b0c55343828
  '''
      }
    }

  }
}