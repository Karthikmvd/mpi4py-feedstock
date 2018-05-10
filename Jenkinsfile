pipeline {
    agent {
        docker { image 'condaforge/linux-anvil' }
    }
    stages {
        stage('Test') {
            steps {
                echo 'Building..'
                yum install -y wget openssh-clients bzip2
                sh 'ci_support/run_docker_build.sh'
                wget https://repo.continuum.io/archive/Anaconda3-5.1.0-Linux-ppc64le.sh
                sh Anaconda3-5.1.0-Linux-ppc64le.sh -b -p /opt/conda
            }
        }
    }
}
