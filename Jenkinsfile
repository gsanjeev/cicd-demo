pipeline
 {
  agent any
	  stages {
		   stage('Build Application'){
			   steps{
			   	bat 'mvn clean install -DskipTests'
			   }
		   } 
		   stage('Deploy Application to CloudHub'){
			   steps{
			   	bat 'mvn package deploy -DmuleDeploy -DskipTests'
			   }
		   }	   

	  }
 }