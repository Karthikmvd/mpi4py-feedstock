pipeline {
    agent {
        docker { image 'condaforge/linux-anvil' }
    }
    stages {
        stage('Test') {
            steps {
                echo 'Building..'
                sh 'ci_support/run_docker_build.sh'
            }
        }
    }
}
