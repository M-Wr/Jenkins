pipeline 
{
    agent any
    stages 
    {
  //       stage('Clean up')
  //       {
  //       	steps 
  //           {
		// sh 'echo removing container'
		// sh 'sudo docker rm -f $(docker ps -aq)' || true
  //           }
  //       }
        stage('Build')
        {
            steps 
            {
		sh 'echo Building container'
		sh 'sudo docker build -t myapp .'
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
