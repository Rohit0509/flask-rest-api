pipeline{
    agent  any 
    stages{
        stage('Install'){
            steps{
               sh 'pip install virtualenv' 
               sh 'virtualenv -p python3 venv'
               sh 'pip install autoenv'
               sh 'source venv/bin/activate'
            }
        }
        stage('Build'){
            steps{
                sh 'pip install -r requirements.txt'
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