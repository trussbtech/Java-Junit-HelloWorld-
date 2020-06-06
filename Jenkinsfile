pipeline {
	agent any
	
    stages {

       stage('SCM') {
		steps {
			echo 'Gathering code from version control'
			git branch: '${branch}', url: 'https://github.com/trussbtech/Java-Junit-HelloWorld-.git'
			}
        }

      stage('build'){
        withMaven(maven: 'mvn') {
            sh "mvn clean compile"
      	}
      }


        stage ('Test') {
          steps {
		   echo "testcode "
		 }
	   }

	}
   
   post {
		always {
			cleanWs()	
		}
	}
}
