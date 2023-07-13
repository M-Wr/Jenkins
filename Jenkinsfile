pipeline 
{
    agent any
    stages 
    {
        stage('Print location and files')
        {
        	steps 
            {
            	sh "pwd"
              sh "ls -la"
            }
        }
        stage('Make new script file')
        {
            steps 
            {
		sh 'touch coolScript.bash'
            }

        }
        stage('script writing')
        {
            steps
            {
            	sh 'version=1'
              sh 'echo"echo Cheers all" > coolScript.bash'
            }

        }
        stage('Running script')
        {
            steps{
              sh 'echo Running script'
			        sh coolScript.bash
			        sh 'readlink -f coolScript.bash'
            }
        }
    }
}
