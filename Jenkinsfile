pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'ci_support/run_docker_build.sh'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                
                
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
