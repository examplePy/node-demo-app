node{
   def app
   stage('Clone repo'){
     checkout scm		
   }	
   stage('Build image'){
     docker.build('test:v1')
   }
   stage('Test'){
     sh 'docker run test:v1 npm run test'
   }
}
