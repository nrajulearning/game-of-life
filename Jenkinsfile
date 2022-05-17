pipeline {
    agent {
  label 'JDK1.8'
}
    triggers {
  pollSCM '* * * * *'
}
    stages{
        stage('One'){ 
            steps{
                 echo 'stage one'
                 echo '$HOSTNAME'
                 sh 'df -h'
            }
           
        }
        stage('Two'){
            agent {
                label 'JDK 11'
            }
            steps{
                 echo 'stage Two'
                 echo '$HOSTS'
                 sh 'cat /etc/os-*'
            }
        }
    }
}