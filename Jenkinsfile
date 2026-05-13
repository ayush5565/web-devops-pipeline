pipeline { 
 
 agent any 
 
 stages { 
 
  stage('Clone Repository') { 
   steps { 
    git branch: 'main',
        url: 'https://github.com/ayush5565/web-devops-pipeline.git',
        credentialsId: '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' 
   } 
  } 
 
  stage('Build Docker Image') { 
   steps { 
    bat 'docker build -t web-devops-app .' 
   } 
  } 
 
  stage('Run Docker Container') { 
   steps { 
        bat 'docker run -d -p 8080:80 --name web-container web-devops-app' 
        } 
    } 
 
 } 
 
} 