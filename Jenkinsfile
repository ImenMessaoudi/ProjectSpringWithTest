pipeline {
    agent any

     environment {
		PATH =  "/opt/apache-maven-3.5.4/bin/:$PATH"
	}

    stages {
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://github.com/ImenMessaoudi/ProjectSpringWithTest.git'
                sh """ mvn clean """
                //bat '.\mvnw clean compile'
            }
        }


         stage('Test') {
            steps {

                sh './mvnw test'
                //bat '.\mvnw test'
            }
        }

      
    }
}
