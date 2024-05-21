pipeline {
    agent any 

    environment {
        IMAGE_NAME = "ash2code/library"
    }

    stages {
     stage("code-checout") {
        steps {
            git 'https://github.com/ash2code/java-jsp-diary.git'
        }
     }
     stage("doker-compose") {
        steps {
            sh "docker-compose up -d"
        }
     } 
     stage("docker-run") {
        steps {
            sh "docker ps -a"
        }
     }      
    }
}
