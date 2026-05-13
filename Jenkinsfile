pipeline { 
 
 agent any 
 
 stages { 
 
  stage('Clone Repository') { 
   steps { 
    git branch: 'main',
        url: 'https://github.com/ayush5565/web-devops-pipeline.git',
        credentialsId: 'ecb6f8d6-4cd3-4976-9281-61820f45043d' 
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