pipeline {
	agent{
	label 'BANISA'
	}
    
    tools { 
        maven 'maven3.5' 
        jdk 'jdk8' 
    }
    stages {
        stage ('seeing environment variables set by me') {
		   agent {
	
	           label 'BANISA'
	
	              }
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
					echo "JAVA_HOME =$(JAVA_HOME)"
                ''' 
            }
        }
		
		
		stage('gitclone'){
		
		
		git 'https://github.com/harisachin200/harirepo.git'
		
		}

        stage ('Artifatc_Maven') {
		     agent {
	
	           label 'BANISA'
	
	              }
            steps {
                sh 'mvn deploy' 
            }
			
        }
    }
}
