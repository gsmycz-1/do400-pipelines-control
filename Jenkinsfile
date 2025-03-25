pipeline {
    agent {
         node {
             label 'nodejs'
         }
    }
    stages {
        stage('Backend Tests') {
            steps {
                sh 'node ./backend/test.js'
            }
        }
        stage('Fronted Tests') {
            steps {
                sh 'node ./frontend/test.js'
            }
        }
    }
}
    