pipeline {
  agent {
    docker {
        image 'espressif/idf:v5.2.1'
    }
  }
	stages {
		stage('Tests') {
			steps {
				sh '/opt/esp/entrypoint.sh idf.py --version'
			}
		}
	}
}