pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                git 'https://github.com/jschelst/spring-petclinic.git'

                sh "./mvnw clean compile"
            }
        }
    }
}
