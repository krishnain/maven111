pipeline
{
    agent any
    stages
    {
        stage('ContinuousDownload')
        {
            steps
            {
                git 'https://github.com/intelliqittrainings/maven.git'
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
                deploy adapters: [tomcat9(credentialsId: '709852eb-f517-4ba1-815b-05a5b7dbe495', path: '', url: 'http://172.31.17.189:8080')], contextPath: 'test1', war: '**/*.war'
            }
        }
        stage('ContinuousTesting')
        {
            steps
            {
                git 'https://github.com/intelliqittrainings/FunctionalTesting.git'
                sh 'java -jar /home/ubuntu/.jenkins/workspace/DeclarativePipeline1/testing.jar'
            }
        }
        stage('ContinuousDelivery')
        {
            steps
            {
                deploy adapters: [tomcat9(credentialsId: '709852eb-f517-4ba1-815b-05a5b7dbe495', path: '', url: 'http://172.31.22.149:8080')], contextPath: 'prod1', war: '**/*.war'
            }
        }
        
        
        
        
        
        
        
        
    }
}
