pipeline{
	agent any
        triggers {
	  pollSCM '* * * * *'
	}

		stages{
			stage(checkout){
				steps{
				checkout scm
				}
			}
			stage(bulid){
				steps{
					sh 'cp/home/sumedh/Downloads/apache-maven-3.9.8/bin/mvn install'
				}
			}
			stage(deploy){
				steps{
					sh 'cp target/GRRAS-01.war /home/sumedh/Downloads/apache-tomcat-9.0.93/webapps'
				}
			}
		}
}
					
