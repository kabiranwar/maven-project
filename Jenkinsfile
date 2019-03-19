pipeline {
    agent any

    
    

    stages{
        stage('Build'){
            steps{
                //bat 'mvn clean package'
                //bat "docker build . -t tomcatwebapp:${env.BUILD_ID}"
                sh 'mvn clean package'
				}
				post{
				success{
				echo 'Now Archieving ...'
				archiveArtifacts artifacts: '**/target/*.war'
				}
            }

        }
    }
	}