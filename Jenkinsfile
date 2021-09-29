pipeline {
 agent any 
   stages {
        stage ('git checkout') {
		   step{
		      git credentialsId: 'github', url: 'https://github.com/vkaneef/onlinebookstore.git'
			}
		}
		stage ('maven build'){
		    step{
			   sh " mvn clean install"
			}
		}
		stage ('deploy"){
		    step{
			    deploy adapters: [tomcat9(credentialsId: 'tomcat', path: '', url: 'http://35.192.182.70:8080/')], contextPath: null, war: '**/*.war'
			}
		}
	}
}
