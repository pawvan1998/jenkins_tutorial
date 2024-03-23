pipeline {
    agent any

    environment {
        SECRET = credentials('TEST')
        TEST_ENV = 'dev'
    }

    stages {
        stage('Example stage 1') {
            steps {
                script {
                    sh "echo ${SECRET}"
                    sh "echo ${TEST_ENV}"
                }
            }
        }
    }
}
