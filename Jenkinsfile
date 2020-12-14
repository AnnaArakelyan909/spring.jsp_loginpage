pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            //args '-v /root/.m2:/root/.m2' 
            args '-u root'
        }
    }
    stages {
        stage('SCM Checkout') {
            steps {
                sh 'git clone https://github.com/AnnaArakelyan909/spring.jsp_loginpage.git'
            }
        }

        stage('Compile-Package') {
            steps {
                def mvnHome = tool name: 'maven-3', type: 'maven'
                sh "${mvnHome}/bin/mvn/package"
            }
        }
    }
}
