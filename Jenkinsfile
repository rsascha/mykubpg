pipeline {
    agent {
        dockerfile {
            filename 'Dockerfile'
            args '-v /var/run/docker.sock:/var/run/docker.sock --group-add docker'
        }
    }
    stages {
        stage ('print infos') {
            steps {
                sh 'docker --version'
                sh 'whoami'
                sh 'groups'
                sh 'docker ps'
                sh 'node --version'
                sh 'npm --version'
                sh 'ng --version'
                sh 'env'
            }
        }

        stage('build process') {
            steps {
                dir ('client/mykubpg-client') {
                    sh 'npm install'
                    sh 'npm run lint'
                    sh 'npm run build'
                    sh 'docker build -t mykubpg-client:latest .'
                    sh 'docker push localhost:5000/mykubpg-client:latest'
                }
            }
        }

    }
}