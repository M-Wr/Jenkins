pipeline 
{
    agent any
    stages 
    {
        stage('Build')
        {
        	steps 
            {
            	sh "pwd"
                sh "ls -la"
            }
        }
        stage('Launch')
        {
            steps 
            {
		sh 'touch coolScript.bash'
	        sh 'version=1'
                sh 'echo "echo Cheers all" > coolScript.bash'
            }

        }

        stage('Test')
        {
            steps{
              sh 'echo Running script'
	      sh 'chmod +x coolScript.bash'
	      sh './coolScript.bash'
	      sh 'readlink -f coolScript.bash'
            }
        }
	 stage('Deploy')
        {
            steps{
              sh 'echo Running script'
	      sh 'chmod +x coolScript.bash'
	      sh './coolScript.bash'
	      sh 'readlink -f coolScript.bash'
            }
        }
    }
}
