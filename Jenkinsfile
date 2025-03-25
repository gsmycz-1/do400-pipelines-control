pipeline {
    agent {
         node {
             label 'nodejs'
         }
    }
    parameters {
        booleanParam(name: "RUNèFRONTEND_TESTS", defaultValue: true)
    }
    stages {
        stage('Run Tests') {
            parallel {
                stage('Backend Tests') {
                    steps {
                        sh 'node ./backend/test.js'
                    }
                }
                stage('Fronted Tests') {
                    when { expression { params.RUN_FRONTEND_TESTS } }
                    steps {
                        sh 'node ./frontend/test.js'
                    }
                }
            }
    
        }
    }
}
    