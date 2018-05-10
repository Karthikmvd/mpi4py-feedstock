pipeline {
     agent {
        docker any
          }
    stages {
        stage('Build') {
           steps {
                echo 'Building..'
                sh 'ci_support/run_docker_build.sh'
            }
        }
    }
}
