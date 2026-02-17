pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "maven3912"
    }

    stages {
        stage('echo maven') {
            steps {
                sh 'echo Print Maven Version'
                sh 'mvn --version'
            }
        }
        
         stage('Build') {
            steps {
               // git branch: 'main', url: 'https://github.com/NaveenAWSDevOps/jenkins-hello-world.git'
                sh 'mvn clean package -DskipTests=true'
            }
        }
        
         stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        
    }
    
}
