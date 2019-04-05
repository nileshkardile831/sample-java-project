pipeline{
        agent any
  stages{
        stage('Deploy to tomcat container'){
                steps{ 
                        echo 'This is declarative pipeline. File is executing from Git'
                        
                        sshagent(credentials: ['Deploy_Pipeline'], ignoreMissing: true) {
                               sh 'scp -o StrictHostKeyChecking=no target/*.war ec2-user@172.31.24.168:/opt/tomcat/webapps'
                           }
                     }
                }
        }
}
