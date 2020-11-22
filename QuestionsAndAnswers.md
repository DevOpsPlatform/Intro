*Jenkins Pipeline Script*:

Example-1:

pipeline {
      stages{
            stage('build'){
                 steps{
                       println "Hello Build"
                 } 
            }
      }
}
