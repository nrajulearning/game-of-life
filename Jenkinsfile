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
            }
           
        }
        stage('Two'){
            steps{
                 echo 'stage Two'
            }
        }
    }
}