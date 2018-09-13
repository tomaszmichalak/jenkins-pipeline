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
        stage('Build') {
            steps {
                sh 'mvn -Dmaven.test.failure.ignore=true install'
            }
            post {
                success {
                    junit 'target/surefire-reports/**/*.xml'
                }
            }
        }
    }
}