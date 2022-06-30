pipeline {
    agent any
    
    stages{
	
	stage('Build'){

	    steps{

	        echo 'Building...'
		sh './gradle build'	    
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

