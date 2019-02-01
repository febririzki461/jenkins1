pipeline {
    agent { dockerfile true }
    stages {
	stage('Checkout'){
	    steps {
                  echo 'Checking out SCM'
                  checkout scm
            }
	}
	stage('Pre Test'){
	    steps {
                    echo 'Pulling Dependencies'
		    withEnv(['PATH+EXTRA=/usr/sbin:/usr/bin:/sbin:/bin']) {  
                    sh ''' go version '''  
            	  }
	      }
	}
    }
}
