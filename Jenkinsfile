pipeline {
  agent any

  tools {
    // Install the Maven version configured as "M2_HOME" and add it to the path.
    maven "mavenp"
  }

  stages {
    
	
	
	stage('Clone') {
      steps {
        // Get some code from a GitHub repository
         git branch: "master", url: "https://github.com/VenkatSevya/boxfuse-sample-java-war-hello.git"
		
}
}
	stage('Compile') {
	     steps {
	         sh "mvn clean package"
	     }
	}
	stage('Test') {
	    steps {
	        sh "mvn clean verify -DskipITs=true',junit '**/target/surefire-reports/TEST-*.xml'archive 'target/*.war"

	    }
	}
  }
}	
