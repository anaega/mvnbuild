node{
	stage('checkout'){
        	checkout scm
	}
	stage('build'){
		sh "mvn clean install"
		sh "ls ./target"
	}
	stage('artifactc creation'){
		archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false
	}
	properties([
       		 [$class: 'CopyArtifactPermissionProperty', projectNames: '*'],
        	pipelineTriggers([])])

}
