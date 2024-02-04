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
        sh '''mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://65.0.56.175:9000 \\
  -Dsonar.token=sqp_f12c2298d77b7916325eff3c2ad42b0c55343828'''
      }
    }

  }
}