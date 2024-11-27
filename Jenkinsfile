pipeline
{
    agent any
    stages
    {
        stage('contdownload')
        {
            steps
            {
               git 'https://github.com/sudarshansw7/mymaven.git'
            }
        }
        stage('contbuild')
        {
            steps
            {
             sh 'mvn package'
            }
        }
        stage('contdeployment')
        {
            steps
            {
                deploy adapters: [tomcat9(credentialsId: '1babbd2e-9c0a-42f0-b6fd-bf449bd5e109', path: '', url: 'http://172.31.17.145:8080')], contextPath: 'webapp', war: '**/*.war'
            }
        }
        
    }
    
}
