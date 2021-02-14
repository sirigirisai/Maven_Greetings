pipeline{
    agent any
    stages{
		stage('GIT'){
			steps{
			git url:"https://github.com/sirigirisai/Maven_Greetings.git"
			}
		}
        stage('SonarQube analysis 1') {
            steps {
			   withSonarQubeEnv('sonarserver') {
                sh 'mvn clean package sonar:sonar'
				}
            }
        }
	}
}