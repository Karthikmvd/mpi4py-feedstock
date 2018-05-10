pipeline {
     agent {
        docker { image 'condaforge/linux-anvil' }
          }
    stages {
        stage('Test') {
            
           
            steps {
                echo 'Building..'
                sh 'yum install -y wget openssh-clients bzip2'
                sh 'wget https://repo.anaconda.com/archive/Anaconda3-5.1.0-Linux-x86_64.sh'
                sh 'sh Anaconda3-5.1.0-Linux-x86_64.sh -b -p /opt/conda  -u'
                sh 'conda build recipe'
            }
        }
    }
}
