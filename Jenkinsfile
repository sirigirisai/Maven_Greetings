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
  -Dsonar.login=d4451a4b26314edc02c7f3c5ffd5c079e9c7029a'
	  }
            }
        }
	}
}