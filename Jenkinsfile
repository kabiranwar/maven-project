pipeline {
    agent any

    environment{
        my_tag = "c:\\temp"
        //my_tag = my_tag
    }
     
    

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
				archieveArtifacts artifacts: '**/target/*.war'
				}
            }

        }
    }
	}