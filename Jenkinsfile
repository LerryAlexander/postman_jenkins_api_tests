pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh label: 'API Collection Tests', script: 'newman run /postman_jenkins_api_tests/tests/postman_tests_collection.json -e /postman_jenkins_api_tests/environment/postman_environment.json -d /postman_jenkins_api_tests/tests/data.json --suppress-exit-code'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}