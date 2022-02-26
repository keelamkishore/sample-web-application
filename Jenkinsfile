currentBuild.displayName = "Final_Demo # "+currentBuild.number

   def getDockerTag(){
        def tag = sh script: 'git rev-parse HEAD', returnStdout: true
        return tag
        }
        

pipeline{
        agent any  
	tools {
		maven 'maven3.8'
	}
        stages{
		stage('git clone'){
			git clone https://github.com/DeekshithSN/sample-web-application.git
		}
		stage('build with maven'){
			sh 'mvn clean install package'
		}
