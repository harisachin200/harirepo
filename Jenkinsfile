node('BANISA') {
   def mvnHome
   stage('Preparation') { // for display purposes
      git 'https://github.com/harisachin200/harirepo.git'
            
      mvnHome = tool 'maven3.5'
   }
   stage('Build') {
      // Run the maven build
      if (isUnix()) {
         sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean deploy"
      } else {
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
   }
   
}
