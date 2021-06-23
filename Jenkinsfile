pipeline {
    agent any
    stages { 
        stage("build") {
            steps {
                sh 'npm install'
                sh 'npm run build'
				}
			}	
			stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './jenkins/scripts/kill.sh'
				}
			
			}
		}	
	}
	