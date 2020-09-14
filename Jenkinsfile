pipeline
 {
  agent any
	  stages {
		   stage('Build Application'){
			   steps{
			   	bat 'mvn clean install'
			   }
		   }	   
		   stage('Deploy Application to CloudHub'){
			   steps{
			   	bat 'mvn package deploy -DmuleDeploy'
			   }
		   }	   
		   stage('Perform Regression Testing'){
			   steps{
			   	bat 'newman run F:\\work\\ulework\\jenkins\\postman\\cicd-demo.postman_collection.json --disable-unicode'
			   }
		   }
	  }
 }