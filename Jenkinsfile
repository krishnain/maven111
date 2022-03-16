@Library('mylibrary')_
pipeline
{
    agent any
    stages
    {
        stage('ContDownload_Master')
        {
            steps
            {
                script
                {
                    cicd.newGit("https://github.com/krishnain/maven111.git")
                }
            }
        }
        stage('ContBuild_Master')
        {
            steps
            {
                script
                {
                    cicd.newBuild()
                }
            }
        }
        stage('ContDeploy_Master')
        {
            steps
            {
                script
                {
                    cicd.newDeploy("http://172.31.17.189:8080","testapp")
                }
            }
        }
        stage('ContTesting_Master')
        {
            steps
            {
                script
                {
                    cicd.newGit("https://github.com/intelliqittrainings/FunctionalTesting.git")
                    cicd.newTest("Pipelinewithlibraries")
                    
                }
            }
            
        }
        stage('ContDelivery_Master')
        {
            steps
            {
                script
                {
                    cicd.newDeploy("http://172.31.22.149:8080","prodapp")
                }
            }
        }
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
    }
}
