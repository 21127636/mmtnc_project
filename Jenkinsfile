pipeline {
    agent any
    stages 
    {
        stage ('Pull Githubrepository') 
        {
            steps 
            {
                git 'https://github.com/21127636/mmtnc_project.git'
            }
        }
        stage ('Build and push Docker image to Docker Hub')
        {
            step
            {
                withDockerRegistry(credentialsId: 'dockerhub', url:"")
                {
                    bat 'docker build -t 21127636/mmtnc_project .'
                    bat 'docker push 21127636/mmtnc'
                }

            }
            
        }
    }
}