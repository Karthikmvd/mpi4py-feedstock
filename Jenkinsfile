pipeline {
    agent none
    stages {
        stage('Test') {
            
            agent {
        docker { image 'condaforge/linux-anvil' }
          }
            steps {
                echo 'Building..'
                sh 'yum install -y wget openssh-clients bzip2'
                sh 'wget https://repo.continuum.io/archive/Anaconda3-5.1.0-Linux-ppc64le.sh'
                sh 'conda build recipe'
            }
        }
    }
}
