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
                label 'JDK11'
            }
            steps{
                 echo 'stage Two'
                 echo '$HOSTNAME'
                 sh 'cat /etc/os-*'
            }
        }
    }
}