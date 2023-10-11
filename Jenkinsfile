pipeline{
   agent any
   stages{
      stage("mvn build and sonar quality check") {
         steps{
	 	withCredentials([string(credentialsId: 'Sonar-token', variable: 'sonar')]) {
    		sh "mvn sonar:sonar -Dsonar.projectKey=Javaweb_e2e -Dsonar.host.url=http://172.31.12.148:9000"
		}
  	 }
      }	
   } 
}
	 	
