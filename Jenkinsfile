pipeline {
    agent any
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
          sh '''
          go version
          '''          
                    //or -update
                    //sh 'cd ${GOPATH}/src/cmd/project/ && dep ensure' 
            }
	  }
	}
    }
}
