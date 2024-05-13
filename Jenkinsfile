pipeline {
    agent {
        docker {
            image 'espressif/idf:v5.2.1'
            args '-e HOME=/tmp'
        }
    }
    stages {
        stage('Build') {
            steps {
                dir('src') {
                    sh '/opt/esp/entrypoint.sh idf.py set-target esp32s3'
                    sh '/opt/esp/entrypoint.sh idf.py build'
                }
            }
        }
    }
}