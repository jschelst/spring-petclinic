pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                git 'https://github.com/jschelst/spring-petclinic.git'

                sh "./mvnw clean compile"
            }
        }
        stage('Scan') {
            steps {
                withSonarQubeEnv(installationName: 'newsonarserver') {
                    sh './mvnw clean org.sonarsource.scanner.maven:sonar-maven-plugin:3.9.1.2184:sonar'
                    //sh './mvnw clean sonar:sonar'
                }
            }
        }
    }
}
