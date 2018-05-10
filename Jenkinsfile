pipeline {
     agent {
        docker { image 'condaforge/linux-anvil' }
          }
    stages {
        stage('Test') {
            
           
            steps {
                echo 'Building..'
                sh 'yum install -y wget openssh-clients bzip2'
                sh 'wget https://repo.continuum.io/archive/Anaconda3-5.1.0-Linux-ppc64le.sh'
                sh 'sh Anaconda3-5.1.0-Linux-ppc64le.sh -b -p /opt/conda  -u'
                sh 'conda build recipe'
            }
        }
    }
}
