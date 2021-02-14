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
                sh 'mvn sonar:sonar \
  -Dsonar.projectKey=greet \
  -Dsonar.host.url=http://localhost:9000 \
  -Dsonar.login=505199b16d2b8853fc6618fe353286248d08a8e3'
				}
            }
        }
	}
}