pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M398"
    }

    stages {
        stage('Echo version') {
            steps {
                sh 'echo Print Maven Version'
                sh 'mvn -version'
            }
        }
        
        stage('Build') {
            steps {
                //Get some code from GitHub repository
                // git branch: 'main', url: 'https://github.com/JacksonMlk/jenkins-hello-world.git'
                
                // Run Maven Package CMD
                sh "mvn clean package -DskipTests=true"
            }
            
        }
        
        stage('Unit test') {
            steps {
                sh "mvn test"
            }
        }
    }
}
