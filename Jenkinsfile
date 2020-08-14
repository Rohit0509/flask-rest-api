pipeline{
    agent  any 
    stages{
        stage('Checkout'){
            steps{
               sh "git git@github.com:Rohit0509/flask-rest-api.git"
            }
        }
        stage('Build'){
            steps{
                sh 'echo "Building"'
            }
        }

        stage('Deploy'){
            steps{
                sh 'echo "Deploy"'
            }
        }
    }
}