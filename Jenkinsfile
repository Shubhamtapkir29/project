pipeline {
agent {
label {
		label "slave-1"
		customWorkspace "/mnt/project-myapp"
		
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
						
						sh "mvn clean package"
			
			}
			
		
		}
		
		stage ('COPY_WAR_TO_Server'){
		
				steps {
						
						sh "scp -r target/LoginWebApp.war saccount@10.0.2.51:/data/project/wars"

						}
				
				}
	
	
	
	}
		
}
