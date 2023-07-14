pipeline 
{
    agent any
    stages 
    {
        stage('Clean up')
        {
        	steps 
            {
		sh 'sudo docker login -u maxwellwri1 -p J44hK@2d3!'
            }
        }
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
