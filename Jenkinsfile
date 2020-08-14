pipeline{
    agent  any 
    stages{
        stage('Install'){
            steps{
               sh 'virtualenv venv'
               sh 'pip3 install autoenv'
            }
        }
        stage('Build'){
            steps{
                sh 'ls -l'
                sh 'sudo ./venv/bin/activate'
                sh 'pip3 install -r requirements.txt'
                sh 'python manage.py db upgrade'
            }
        }
        stage('Deploy'){
            steps{
                sh 'echo "Deploy"'
                sh 'python run.py'
            }
        }
    }
}