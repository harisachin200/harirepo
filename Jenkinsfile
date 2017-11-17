pipeline {
	tools{ 
        maven 'maven3.5' 
        jdk 'jdk8'
	}
    stages{
        stage('seeing environment variables set by me') {
		node('BANISA'){
            steps {
                sh '''
                    echo "PATH = ${PATH}"
		    echo "M2_HOME = ${M2_HOME}"
		    echo "JAVA_HOME =$(JAVA_HOME)"
                ''' }
	}
	}
	    stage('gitcode'){
		    node('BANISA'){
            checkout scm
		    }
			
        }
	    
	    
	    stage('Artifatc_Maven'){
		    node('BANISA'){
            steps {
                sh 'mvn deploy'
	    }
		    }
			
        }
	    
	    
    }
}
