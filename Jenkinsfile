pipeline {
    agent any

    stages {

	stage('Checkout'){
        	echo 'Checking out SCM'
                checkout scm
        }
                
        stage('Pre Test'){
                    echo 'Pulling Dependencies'
            
                    sh 'go version'
                    sh 'go get -u github.com/gin-gonic/gin'
                    
                    //or -update
                    sh 'cd ${GOPATH}/src/cmd/project/ && dep ensure' 
        }

    }
}