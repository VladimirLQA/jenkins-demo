@Library('Demo') _

def config = [
    name: 'Viva',
    dayOfWeek: getDayOfWeek()
]

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
                helloWorldExternal(config)
            }
        }
    }
}

def getDayOfWeek() {
    return new Date().format('EEEE')
}
