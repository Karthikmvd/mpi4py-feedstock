pipeline {
    agent {
        docker { image 'condaforge/linux-anvil' }
    }
    stages {
        stage('Test') {
            steps {
                echo 'Building..'
                'yum install -y wget openssh-clients bzip2'
                sh 'ci_support/run_docker_build.sh'
            }
        }
    }
}
