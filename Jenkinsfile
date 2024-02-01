node('built-in')
{
    stage('ContDownload')
    {
        cicd.newDownload("maven.git")
    }
    stage('ContBuild')
    {
        cicd.newBuild()
    }
    stage('ContDeployment')
    {
        cicd.newDeploy("ScriptedPipelinewithsharedlibraries","172.31.32.68","testapp")
    }
    stage('ContTesting')
    {
         cicd.newDownload("FunctionalTesting.git")
         cicd.runSelenium("ScriptedPipelinewithsharedlibraries")
    }
    stage('ContDelivery')
    {
        cicd.newDeploy("ScriptedPipelinewithsharedlibraries","172.31.32.210","prodapp")
    }
    
    
    
    
}
