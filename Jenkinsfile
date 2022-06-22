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
            steps {
                echo 'Testing'
                input('Do you want to proceed? ')
            }
        }
        stage('Deploying') {
            steps {
                echo 'Deploying'
            }
        }
    }
}
