@Library('shared-library') _

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
        // stage('Run helloWorld.js') {
        //     steps {
        //         sh '''
        //             echo "Running helloWorld.js..."
        //             node helloWorld.js
        //         '''
        //     }
        // }

        stage('Run shared library helloWorld var') {
            steps {
                helloWorld()
            }
        }
    }
}