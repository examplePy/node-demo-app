node{
   def app
   stage('Clone repo'){
     checkout scm		
   }	
   stage('Build image'){
     docker.build('test:v1')
   }
   stage('Test'){
     app.inside{
       sh 'npm install'
       sh 'npm test' 
     }
   }

}
