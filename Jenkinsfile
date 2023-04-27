node{
	stage('checkout'){
        	checkout scm
	}
	stage('example'){
		sh "mvn clean install"
		sh "ls ./target"
	}
}
