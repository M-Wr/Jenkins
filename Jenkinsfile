pipeline 
{
    agent any
    stages 
    {
        // stage('Clean up')
        // {
        // 	steps 
        //     {
		
        //     }
        // }
        stage('Build')
        {
            steps 
            {
		sh 'echo Building container'
		sh 'docker build -t myapp .'
            }

        }

        stage('Deploy')
        {
            steps{
              sh 'sudo docker run -d -p 80:5500 --name myapplication myapp'
            }
	}
    }
}
