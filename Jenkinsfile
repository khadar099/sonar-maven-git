pipeline {
	agent any
stages {
    stage('Clone repo'){
        git credentialsId: 'gitcreds', url: 'https://github.com/khadar099/sonar-maven-git.git'
    }
    stage('SonarQube analysis') {       
        withSonarQubeEnv('Sonar-Server-7.8') {
       	sh "mvn sonar:sonar"    	
    		}
    	}
   }
}
