pipeline {
    agent any

    stages {
        stage('Git download') {
            steps {
                echo 'Downloading git code...'

                git url: 'https://github.com/srilatha71/Jenkins-maven-CI-Pipeline.git',
                    branch: 'main',
                    credentialsId: 'github-token'

                echo 'Download completed.'
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
