pipeline {
    agent any
    
    stages{
	
	stage('Build'){

	    steps{

	        echo 'Building...'
		sh './gradlew build'	    
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

