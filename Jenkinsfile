pipeline {
    agent any

    stages {
        stage('Init') {
            steps {
                sh '''
                    echo "Initializing..."
                    node -v
                    npm -v
                '''
            }
        }
    }
}