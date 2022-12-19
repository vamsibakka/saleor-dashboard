pipeline{
    agent any
    stages {
        stage('vcs'){
            steps {
                git branch:'main',url:'https://github.com/vamsibakka/saleor-dashboard.git'             
            }
        }
        stage('docker image build'){
            steps {
                sh 'docker image build -t vamsibakka/saleor-dashboard:DEV'
            }

        }
        stage('push image'){
            steps {
                sh 'docker image push vamsibakka/saleor-dashboard:DEV'
            }
        }
    }
}