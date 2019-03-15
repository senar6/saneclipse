// Powered by Infostretch 

timestamps {

node () {

	stage ('example-maven-project - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '8cc7275d-866e-4436-8bc5-935610de3d14', url: 'https://github.com/senar6/saneclipse.git']]]) 
	}
	stage ('example-maven-project - Build') {
 			// Maven build step
	//withMaven(maven: 'Maven3.5.2') { 
 			if(isUnix()) {
 				sh "mvn clean verify " 
			} else { 
 				bat "mvn clean verify " 
			} 
 		//} 
	}
}
}
