pipeline {
    agent any

   stage('Checkout') {
    steps {
        git branch: 'main',
            credentialsId: 'jenklin',
            url: 'https://github.com/muniprakash04/carwebsite.git'
    }
}

        stage('Deploy') {
            steps {
                sh '''
                sudo rm -rf /var/www/html/*
                sudo cp -r * /var/www/html/
                sudo systemctl restart nginx
                '''
            }
        }
    }
}
