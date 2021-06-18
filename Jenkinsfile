pipeline{
    agent any
        stages{
            stage('build'){
                steps {
                    sh "mvn clean package"
                }
            }
            stage('deploy'){
                steps {
                    deploy adapters: [tomcat7(credentialsId: '0c471957-1eda-4edd-85d7-55d5610b6b24', path: '', 
                    url: 'http://ec2-18-116-112-77.us-east-2.compute.amazonaws.com:8080/')], 
                    contextPath: 'javawebapp', war: '**/java-web-project.war'
                }
            }
                
            }
        
    }
