pipeline {
  agent any

  stages {
      stage('Build Artifact') {
            steps {
              sh "mvn clean package -DskipTests=true"
              archive 'target/*.jar' //therefore they can be downloaded later
            }
        }

      stage('Unit Tests') {
            steps {
              sh "mvn test"
            }
        }   
    }
}