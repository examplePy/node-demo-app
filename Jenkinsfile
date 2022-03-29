node{
   def app
   stage('Clone repo'){
     checkout scm		
   }	
   stage('Build image'){
     docker.build('test:v1')
   }
   stage('Test'){
     nodejs(nodeInstallationName:'nodejs'){
     sh 'npm install'
     sh 'npm test'
   }

}
