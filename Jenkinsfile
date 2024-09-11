pipeline {
 agent any
    stages {
        stage('build'){
            steps{
             sh "docker build -t hazemhashem100/web2:${BUILD_NUMBER} ."
            }
        }
        stage('cd'){
            steps{
 
             sh  "docker run -d -p 80:80 --name=web hazemhashem100/web2:${BUILD_NUMBER}"
              
            }
        }
        
    }
}
