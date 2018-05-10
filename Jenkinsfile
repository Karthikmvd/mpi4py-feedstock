pipeline {
     agent {
        docker { image 'condaforge/linux-anvil' }
          }
    stages {
        stage('Test') {
            
           
            steps {
                sh 'who am i 
                echo 'Building..'
                sh 'yum install -y wget openssh-clients bzip2'
                sh 'wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh'
                sh 'sh Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda  -u'
                sh 'who am i' 
                sh '/opt/conda/bin/conda build recipe'
            }
        }
    }
}
