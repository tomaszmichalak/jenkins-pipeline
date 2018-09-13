pipeline {
    agent any
    tools { 
        maven 'Maven 3.5.4'
        jdk 'jdk10'
    } 
    stages {
        stage('Init') { 
            steps {
         	      echo "PATH = ${PATH}"
                echo "M2_HOME = ${M2_HOME}"        
            }
        }
    }
}