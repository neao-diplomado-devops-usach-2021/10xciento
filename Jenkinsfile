pipeline {
    agent any
    stages {
        stage('Clean') {
            steps {
                sh 'docker run --rm -v $(pwd):/code --workdir /code maven mvn clean'
            }
        }

        stage('Compile') {
            steps {
                sh 'docker run --rm -v $(pwd):/code --workdir /code maven mvn compile'
            }
        }

        stage('Test') {
            steps {
                sh 'docker run --rm -v $(pwd):/code --workdir /code maven mvn test'
            }
        }
    }
}
