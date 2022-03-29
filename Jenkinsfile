pipeline {
    agent any

    stages {
        stage('continious download') {
            steps {
           git 'https://github.com/kliakos/sparkjava-war-example.git'
            }
        }
        stage('continious build') {
            steps {
            sh 'mvn install'
            }
        }
        stage('continious deployment') {
            steps {
            sh 'sshpass -p "divya" scp target/sparkjava-hello-world-1.0.war root@172.17.0.3:/var/lib/apache-tomcat-9.0.56/webapps'
            }
        }
    }
}

