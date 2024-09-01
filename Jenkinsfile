pipeline{
	agent any
        triggers {
	  pollSCM '* * * * *'
	}

		stages{
			stage(checkout){
				steps{
					git 'git \'https://github.com/wakharesumedh/GRRAS-01.git\''
				}
			}
			stage(bulid){
				steps{
					build 'mvn install'
				}
			}
			stage(deploy){
				steps{
					sh 'cp target/GRRAS-01.war /home/sumedh/Downloads/apache-tomcat-9.0.93/webapps
				}
			}
		}
}
					
