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
        
        stage('Deploy') {
            steps {
                sh 'cd /var/lib/jenkins/workspace/My_Project/target/'
                sh 'BUILD_ID=abbas nohup java -Dserver.port=9080 -jar demo-docker.jar &'
            }
        }
    }
}
