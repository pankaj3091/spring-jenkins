pipeline {
    agent any
    stages{
	stage('Checkout'){
		steps{
			checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'd3470348-6cbb-4910-8dc1-0c4b549ed444', url: 'https://github.com/pankaj3091/SimpleApp.git']]])
			}
		}
        stage('Build'){
            steps{
                bat 'mvn clean package'
		 }
        }
    }
}
