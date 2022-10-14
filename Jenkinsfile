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
        stage("build image") {
           
           
            steps {
                script {
                    buildImage "REPO NAme:3.00"
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
