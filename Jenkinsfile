node('BANISA') {
   tools{ 
        maven 'maven3.5' 
        jdk 'jdk8'
	}
   
   stage('git clone') { 
   // cloning git repository
      git 'https://github.com/harisachin200/harirepo.git'
            
			}
   stage('ArtifactDep') {
      // Run the maven build
      if (isUnix()) {
         sh " mvn clean"
      } else {
         bat(/"${mvnHome}\bin\mvn"  clean deploy/)
      }
   }
   
}
