pipeline{
    agent any
    // here any -  any available server that jenkins itself can connect to 
    // that means the agent is current server only
    // label 'win_server'  - this is server name
    
    tools{
        maven 'mymaven'
    }
    
    stages{
        
        stage('checkout code'){
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        stage('complie code'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('Review code'){
            steps{
               sh 'mvn pmd:pmd'
            }
        }
        stage('Test code'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package code'){
            steps{
                sh 'mvn package'
            }
	}
            stage('Deploy code'){
            steps{
                echo 'Deployed'
            }
        }
    }
}
