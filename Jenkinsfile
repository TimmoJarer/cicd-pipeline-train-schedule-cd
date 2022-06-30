pipeline {
    agent any
    
    stages{
	
	stage('Build'){

	    steps{

	        echo 'Building...'
		sh './gradlew --version'	    
  	    }
	}

	stage('Test'){

	    steps{

	        echo 'Testing...'
    	    }
	}

	stage('Deployment'){

	    steps{

      	        echo 'Deploying...'
	    }
	}

    }

}

