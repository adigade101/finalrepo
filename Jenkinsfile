pipeline { 
    environment { 
        registry = "adigade101/finalrepo"
    }
    agent any 
    stages { 
        stage('Cloning our Git') { 
            steps { 
                git branch:'main', url: 'https://github.com/adigade101/finalrepo.git' 
            }
        } 
        stage('Running terraform') { 
            steps { 
                echo 'Run terraform file'
                sh "cd terraform/"
                sh "terraform init"
                sh "terraform validate"
                sh "terraform fmt"
                sh "terraform apply -auto-approve" 
            }
        }
       
    }
}