pipeline{
    agent  any 
    stages{
        stage('Install'){
            steps{
               sh 'pip3 install virtualenv' 
               sh 'virtualenv -p python3 venv'
               sh 'pip3 install autoenv'
               sh 'source venv/bin/activate'
            }
        }
        stage('Build'){
            steps{
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