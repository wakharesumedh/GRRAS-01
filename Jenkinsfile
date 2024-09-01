pipeline {
    agent any
    environment{
        JAVA_HOME = '/home/sumedh/Downloads/jdk-11.0.24'
    }
triggers {
  pollSCM '* * * * *'
}


    stages {
        stage('checkout') {
            steps {
                checkout scm
            }
        }
        stage('BUILD'){
            steps{
                sh '/home/sumedh/Downloads/apache-maven-3.9.8/bin/mvn install'
            }
        }
        stage('DEPLOYMENT'){
            steps{
                sh 'cp target/GRRAS-01.war /home/sumedh/Downloads/apache-tomcat-9.0.93/webapps'
            }
        }
    }
}
