node{
   def app
   stage('Clone repo'){
     checkout scm		
   }	
   stage('Build image'){
     docker.build('test:v1')
   }
   stage('Test'){
     steps{
	sh 'node --version'
     }
   }
}
