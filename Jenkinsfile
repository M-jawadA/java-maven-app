//CODE_CHANGES = getGitChanges()
@Library("jenkins-shared-library")_
pipeline {
    agent any
    stages {
        stage("build") {
            
            steps {
                script {
                    buildJar()
                }
            }
        }
        stage("docker login and build image") {
           
           
            steps {
                script {
                    buildImage()
                    dockerLogin()
                    dockerPush "my image NAME"
                }
            }
        }
        stage("deploy") {
            steps {
                      echo "deploying application..."
           
               
            }
        }
       
    }   
}
