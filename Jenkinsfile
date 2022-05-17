pipeline {
    agent any
    triggers {
  pollSCM '* * * * *'
}
    stages{
        stage('One'){ 
            agent {
                label 'JDK1.8'
            }
            steps{
               echo 'stage one'
               echo '$HOSTNAME'
               sh 'cat /etc/*-release'
               sh 'mvn clean package'
           }
        }
        stage('Two'){
            agent {
                label 'JDK11'
            }
            steps{
                echo 'stage Two'
                echo '$HOSTNAME'
                sh 'cat /etc/os-*'
                sh 'mvn clean package'
            }
        }
    }
}