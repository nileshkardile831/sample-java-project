pipeline{
        agent any
  stages{
        stage('Deploy to tomcat container'){
                steps{ 
                        echo 'This is declarative pipeline. File is executing from Git'
                        
                        sshagent(['c1aaa18f-e59a-441c-92c0-00190f402bcb']) {
                               sh 'scp -o StrictHostKeyChecking=no sample.war ec2-user@172.31.24.168:/opt/tomcat/webapps/'
                           }
                     }
                }
        }
}
