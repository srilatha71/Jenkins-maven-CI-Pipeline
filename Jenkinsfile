pipeline {
    agent any

    stages {
        stage('Git download') {
            steps {
                echo 'Download git code.'
                git 'https://github.com/your-repo/hello-world-maven.git'
                echo 'Downloaded the code completed.'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
       stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
