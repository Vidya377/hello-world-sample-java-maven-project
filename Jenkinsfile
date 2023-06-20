 pipeline {
    agent any
    
    stages {
        
        stage('deploy') {
            steps {
                sshagent(['deployment_tomcat']) {
                sh "scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/Maven_Build_Job/webapp/target/webapp.war ec2-user@65.2.125.97:/opt/apache-tomcat-9.0.76/webapps"
                    
                }
                
            }
        }
    }
}
