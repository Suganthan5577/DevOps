pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git url: 'https://github.com/Suganthan5577/DevOps.git', branch: 'main'
            }
        }
        stage('Deploy to NGINX') {
            steps {
                sh '''
                sudo cp index.html /var/www/html/index.html
                sudo systemctl restart nginx
                '''
            }
        }
    }
}
