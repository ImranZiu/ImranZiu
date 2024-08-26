pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/ImranZiu/ImranZiu.git'
            }
        }
        stage('Build') {
            steps {
                script {
                    docker.build("my-node-app")
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    docker.image("my-node-app").run("-p 3000:3000")
                }
            }
        }
    }
}
