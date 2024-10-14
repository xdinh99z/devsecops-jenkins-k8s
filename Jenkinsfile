pipeline {
  agent any
  tools { 
        maven 'Maven_3.6.3'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean'
			}
        } 
  }
}
