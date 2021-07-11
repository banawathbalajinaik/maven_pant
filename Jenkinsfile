pipeline {
    agent any 
    stages {
        stage('git clone') { 
            steps {
                sh'''
                pwd
                rm -rf simple-java-maven-app
                git clone "https://github.com/banawathbalajinaik/simple-java-maven-app.git"
                '''
            }
        }
        stage('clean') { 
            steps {
                sh'''
                cd simple-java-maven-app
                mvn clean
                '''
            }
        }
        stage('compile') { 
            steps {
                sh'''
                cd simple-java-maven-app
                mvn compile
                '''
            }
        }
        stage('test') { 
            steps {
                sh'''
                cd simple-java-maven-app
                mvn test
                '''
            }
        }
    }
}
