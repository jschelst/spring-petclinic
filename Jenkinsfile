pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                git 'https://github.com/jschelst/spring-petclinic.git'

                sh "./mvnw clean compile"
            }
        }
    }
}
