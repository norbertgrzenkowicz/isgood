pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'docker build -t isgood .'
                }
            }
        }
        stage('Run') {
            steps {
                script {
                    sh 'docker run -d -p 3000:3000 --name isgood_container isgood'
                }
            }
        }
    }
}