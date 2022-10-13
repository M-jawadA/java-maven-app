//CODE_CHANGES = getGitChanges()
pipeline {
    agent any
   // environment {
     //   NEW_VERSION = '1.3.0'
       // SERVER_CREDENTIALS = credentials('server-credential')
   // }
    parameters {
        choice(name:'VERSION',choices:["1.1.0","1.2.0","1.3.0"],description:"version to deploy ")
        boleanParam(name:'executeTest',defaultValue: true,description:"bolean to deploy ")
    }
    stages {
        stage("build") {
            
            steps {
               echo "building application..."
                echo "builgin version ${NEW_VERSION}"
            }
        }
        stage("test") {
            when{
                expression {
                    params.executeTest
                }
            }
           
            steps {
                      echo "testing application..."
            }
        }
        stage("deploy") {
            steps {
                      echo "deploying application..."
                echo "deploying version ${params.VERSION}"
                //echo "deploying with ${ SERVER_CREDENTIALS }"
               // withCredentials([
                  //  usernamePassword(credentials:'server-credential',usernameVariable: USER, passwordVariable: PWD)
               // ]){
               //     sh "some script ${USER} ${PWD}"
               // }
            }
        }
       
    }   
}
