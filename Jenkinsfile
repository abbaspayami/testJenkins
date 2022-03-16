pipeline {
    agent any
    stages {
        stage('Git-Checkout') {
            steps {
                echo "checking out from Git Repo"
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}
