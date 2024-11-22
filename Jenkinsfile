pipeline {

    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        GREETING = "Hello jenkins"
    }
    // build
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing.. from web hook'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                    echo 'Here i wrote shell script'
                    env
                """
            }
        }
    }
    //post build
    post {
        always {
            echo "I will always say Hello again!"
        }
        failure {
            echo 'This runs when pipe line is failed, used generaly to send some alerts.'
        }
        success {
            echo ' I will say Helo when piope line is success.'
        }
    }
}