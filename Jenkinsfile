node {
	echo ' Microservice CI/CD Pipeline - API Gateway ' 
	echo " #################### Initiating ${env.BRANCH_NAME} Build #################### "
		
    properties([pipelineTriggers([githubPush()])])
    
    docker.image('maven:3.3.3-jdk-8').inside {
	stage ('Pull Repository') {
		checkout scm
	}
	
	stage('Build Java') {
	    sh "mvn dependency:purge-local-repository"
		sh "mvn clean install"
      	sh 'cp ./target/api-gateway-0.0.1-SNAPSHOT.jar ./api-gateway-0.0.1-SNAPSHOT.jar'
	}
  }
}
