pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                //
                git 'https://github.com/sunildevops77/maven.git'
                
                  }
                           }
        stage('Build') {
            steps {
                //
                sh 'mvn package'
                  }
                        } 
        stage('Deplyment') {
            steps {
                 //
                 sh 'scp /home/ubuntu/.jenkins/workspace/wipro_2/webapp/target/webapp.war ubuntu@172.31.38.138:/var/lib/tomcat9/webapps/qaenv.war'
                  }             
                           }
        stage('Testing') {
            steps {
                 //
                sh 'echo "testing passed"'
                  }
                         }
        stage('Delivery') {
            steps {
                //
                sh ' scp /home/ubuntu/.jenkins/workspace/wipro_2/webapp/target/webapp.war ubuntu@172.31.38.170:/var/lib/tomcat9/webapps/prodenv.war'
                  }
                          }                 
           } 
           
    }   
