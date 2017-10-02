node {
	echo ' Microservice CI/CD Pipeline - API Gateway ' 
	echo "#################### Initiating ${env.BRANCH_NAME} Build ####################"
		
    properties([pipelineTriggers([githubPush()])])
	
	stage ('Pull Repository') {
		checkout scm
	}
}
