pipeline {
    agent any  // 在任意可用节点运行
    stages {
        stage('Checkout') {
            steps {
                checkout scm  // 拉取代码
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building..."'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing..."'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying..."'
            }
        }
    }
}
