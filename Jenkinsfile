pipeline {
agent {
label {
		label "built-in"
		customWorkspace "/mnt/project"
		
		}
		}
		
	stages {
		
		stage ('CLEAN_OLD_M2') {
			
			steps {
				sh "rm -rf /root/.m2/repository"
				
			}
			
		}
	
		stage ('MAVEN_BUILD') {
		
			steps {
						
						sh "mvn clean install"
			
			}
			
		
		}
			
	
	
	}
		
}
