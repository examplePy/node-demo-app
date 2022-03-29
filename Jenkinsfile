node{
   def app
   stage('Clone repo'){
     checkout scm		
   }	
   stage('Build image'){
     app=docker.build('test:v1')
   }
   stage('Test'){
     app.inside{
        sh 'npm install'
        sh 'npm test'
     }  
   }
}
