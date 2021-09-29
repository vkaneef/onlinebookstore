pipeline {
 agent any 
   stages {
        stage ('git checkout') {
		   step{
		      git branch: 'J2EE', credentialsId: 'tomcat', url: 'https://github.com/vkaneef/onlinebookstore.git'
			}
		}
		stage ('maven build'){
		    step{
			   sh " mvn clean install"
			}
		}
	}
}
