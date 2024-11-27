pipeline
{
    agent any
    stages
    {
        stage('ContinuousDownload')
        {
            steps
            {
                git 'https://github.com/sudarshansw7/mymaven.git'
            }
        }
        stage('ContinuousBuild')
        {
            steps
            {
                sh 'mvn package'
            }
        }
        stage('ContinuousDeployment')
        {
            steps
            {
               sh "scp /var/lib/jenkins/workspace/withoutplugin/webapp/target/webapp.war ubuntu@172.31.17.145:/var/lib/tomcat10/webapps/testapp.war"
            }
        }
   
    }
    
}
    
