pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/giriprasanna7/carr-website-1.git'
            }
        }

        stage('Deploy Website') {
            steps {
                sh '''
                sudo cp -r carwebsite-main/carwebsite/* /var/www/html/
                sudo systemctl restart httpd
                '''
            }
        }

    }
}
