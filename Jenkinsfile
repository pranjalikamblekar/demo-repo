pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World this is main branch.'
            }
        }
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
        stage('Test') {
            parallel {
                stage('Unit Tesing') {
                    steps {
                        echo 'Running the unit test..'
                    }
                }
                stage('Integration Testing') {
                    agent any
                    steps {
                        echo 'Runing integration test..'
                    }
                }
            }
        }
    }
}
