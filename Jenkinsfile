pipeline {
    agent any
    tools {
        maven 'Maven'
        jdk "JDK"
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn --version'
                sh 'java --version'
                sh 'javac --version'
                sh 'mvn clean install'
            }
        }
  
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('CompileandRunSonarAnalysis') {
            steps {
                sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=xdinh99z_devsecops-jenkins-k8s -Dsonar.organization=devsecops-jenkins-k8s -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=5bf668218134a552884d189db389aced37f83ab9'
            }
        }
    }
}
