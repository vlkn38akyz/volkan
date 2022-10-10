pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'docker build -t my-nginx .'
            }
        }
        stage('sil') {
            steps {
                echo 'silmek..'
                sh 'docker container rm -f volkan'
            }
        }
        stage('run') {
            steps {
                echo 'running....'
                sh 'docker run -d --name volkan -p 80:80 my-nginx'
            }
        }
    }
}
