pipeline {
    agent any 
    stages {
        stage('git clone') { 
            steps {
                sh'''
                pwd
                rm -rf shell_praticles
                git clone "https://github.com/banawathbalajinaik/shell_praticles.git"
                '''
            }
        }
        stage('clean') { 
            steps {
                sh'''
                cd shell_praticles
                mvn clean
                '''
            }
        }
        stage('compile') { 
            steps {
                sh'''
                cd shell_praticles
                mvn compile
                '''
            }
        }
        stage('test') { 
            steps {
                sh'''
                cd shell_praticles
                mvn test
                '''
            }
        }
    }
}
