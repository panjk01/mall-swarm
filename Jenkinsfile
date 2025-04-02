pipeline {
    agent any  // 在任意可用节点运行
    parameters {
        choice(name: 'ENVIRONMENT', choices: ['dev', 'test', 'prod'], default: 'prod', description: 'Choose the deployment environment')
    }
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
                script {
                    if (params.ENVIRONMENT == 'dev') {
                        echo 'Deploying to Development'
                        // 部署到开发环境的具体命令
                    } else if (params.ENVIRONMENT == 'test') {
                        echo 'Deploying to Test'
                        // 部署到测试环境的具体命令
                    } else if (params.ENVIRONMENT == 'prod') {
                        echo 'Deploying to Production'
                        // 部署到生产环境的具体命令
                    }
                }
            }
        }	
    }
}
