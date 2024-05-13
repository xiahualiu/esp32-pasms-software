pipeline {
    agent {
        docker {
            image 'espressif/idf:v5.2.1'
        }
    }
    stages {
        stage('Build') {
            steps {
                dir('src') {
                    sh '/opt/esp/entrypoint.sh idf.py set-target esp32s3'
                    sh 'CCACHE_CONFIGPATH=/tmp/.ccache /opt/esp/entrypoint.sh idf.py build'
                }
            }
        }
    }
}