node{
   def app
   stage('Clone repo'){
     checkout scm		
   }	
   stage('Build image'){
     docker.build('examplePy/node-demo-app')
   }
   stage('Test'){
     app.inside{
       sh 'npm install'
       sh 'npm test' 
     }
   }

}
