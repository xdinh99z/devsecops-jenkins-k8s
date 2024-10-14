pipeline {
  agent any
  tools { 
        maven 'Maven'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=devsecops-jenkins-k8s -Dsonar.organization=devsecops-jenkins -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=5bf668218134a552884d189db389aced37f83ab9'
			}
        } 
  }
}
