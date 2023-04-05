pipeline {
    agent any

     tools{
    	    maven "M2_HOME"

        }
    	environment {
    	        PATH = "$PATH:/usr/share/maven/bin"
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
