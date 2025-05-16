pipeline {
    agent any
    tools {
        nodejs "nodejs18"
    }
    stages {
        stage('Checkout Code') {
            steps {
                echo 'Checkout Code First time'
                //git branch: 'main', url: 'https://github.com/staticwebdev/react-basic.git'
                git branch: 'main', changelog: false, credentialsId: 'sonusharma85git', poll: false, url: 'https://github.com/sonusharma85indore/react-website.git'
            }
        }
        stage('Install Dependency') {
           
            steps {
                echo 'Install Dependency'
                sh 'node -v'
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                echo 'Build'
                sh 'npm run build'
            }
        }
        stage('Code Coverage') {
            steps {
                echo 'Code Coverage'
            }
        }
        stage('Code Scan') {
            steps {
                echo 'Code Scan'
            }
        }
        stage('Build Artifact') {
            steps {
                echo 'Build Artifact'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
        
    }
}
