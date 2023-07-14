pipeline 
{
    agent any
    stages 
    {
        stage('Clean up')
        {
        	steps 
            {
		sh 'if [ /*docker ps check some value */ ]; then docker stop rabbitmq && docker rm -f rabbitmq fi'
            }
        }
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
              sh 'docker run -d -p 80:5500 --name myapplication myapp'
            }
	}
    }
}
