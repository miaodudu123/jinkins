pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // 方案1：直接使用完整仓库URL（推荐简单项目）
                git url: 'https://github.com/miaodudu123/jinkins.git', branch: 'main'
                
                // 或者方案2：复用全局SCM配置（推荐）
                // checkout scm
            }
        }
        
        stage('Install') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }
        
        stage('Test') {
            steps {
                bat 'pytest'
            }
        }
    }
}
