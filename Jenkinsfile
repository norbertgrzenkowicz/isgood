pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    docker.build('isgood')
                }
            }
        }
        stage('Run') {
            steps {
                script {
                    docker.image('isgood').run('-p 3000:3000')
                }
            }
        }
    }
}