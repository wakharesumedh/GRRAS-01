pipeline{
	agent any
        triggers {
	  pollSCM '* * * * *'
	}
	environment{
		JAVA_HOME = /home/sumedh/Downloads/jdk-11.0.24
	}

		stages{
			stage(checkout){
				steps{
				checkout scm
				}
			}
			stage(bulid){
				steps{
					build 'mvn install'
				}
			}
			stage(deploy){
				steps{
					sh 'cp target/GRRAS-01.war /home/sumedh/Downloads/apache-tomcat-9.0.93/webapps'
				}
			}
		}
}
					
