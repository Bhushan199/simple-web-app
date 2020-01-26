// Powered by Infostretch 

timestamps {

node () {

	stage ('job_for_folder/test1 - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'f9bf7227-ef43-43b3-8ca0-dacbb2b126a7', url: 'https://github.com/Bhushan199/simple-web-app']]]) 
	}
	stage ('job_for_folder/test1 - Build') {
 			// Maven build step
	withMaven { 
 			if(isUnix()) {
 				sh "mvn clean install " 
			} else { 
 				bat "mvn clean install " 
			} 
 		} 
	}
}
}