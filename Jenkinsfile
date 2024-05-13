pipeline {
  agent {
    docker {
        image 'espressif/idf:v5.2.1'
    }
  }
	stages {
		stage('Checkout') {
			steps {
				sh 'ls -al'
			}
		}
	}
}