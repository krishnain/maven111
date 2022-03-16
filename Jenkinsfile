@Library('mylibrary')_
pipeline
{
    agent any
    stages
    {
        stage('ContDownload_Loans')
        {
            steps
            {
                script
                {
                    cicd.newGit("https://github.com/krishnain/maven111.git")
                }
            }
        }
        stage('ContBuild_Loans')
        {
            steps
            {
                script
                {
                    cicd.newBuild()
                }
            }
        }
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
    }
}
