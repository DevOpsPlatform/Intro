The Main aim of this page is to practice Jenkins Pipeline Script.

**Jenkins** Version: Jenkins 2.249.3

**Pipeline** plugin version: 2.6

*Jenkins Pipeline Script*:

*Example-1*:

      pipeline {
            stages{
                  stage('build'){
                       steps{
                             println "Hello Build"
                       } 
                  }
            }
      }

*Output*:

      Running in Durability level: MAX_SURVIVABILITY
      org.codehaus.groovy.control.MultipleCompilationErrorsException: startup failed:
      WorkflowScript: 1: Missing required section "agent" @ line 1, column 1.
         pipeline {
         ^

      1 error

            at org.codehaus.groovy.control.ErrorCollector.failIfErrors(ErrorCollector.java:310)

*Solution*: Agent section is required to start the pipeline.

      pipeline {
          agent any
          stages{
              stage('build'){
                  steps{
                      println "Hello Build"
                  } 
              }
          }
      }
      
also, try this. 

      pipeline {
            agent any
      }
      
Above script also will NOT work. Therefore, minimum 'agent' and 'stages' sections are required to satrt executing the pipeline script.


*Example-2*:

      pipeline {

          agent any

          stages{
              stage('build'){

                  println "Hello Build - outside steps"

                  steps{
                      println "Hello Build - inside steps"
                  }
              }
          }
      }

*Output*: Thrwos error

      org.codehaus.groovy.control.MultipleCompilationErrorsException: startup failed:
      WorkflowScript: 6: Unknown stage section "println". Starting with version 0.5, steps in a stage must be in a ‘steps’ block. @ line 6, column 15.
                 stage('build'){
                 ^
                 
From, we can understand what is minimum required under the "stage" section. Because of under stage "steps" is not only the section we can define. There are many other sections we can define under "stage" section.

*Example-3*: What it is going to print?

      pipeline{
          agent any
          stages{
              stage("Env example-1"){
                  steps{
                      sh 'printenv'
                  }
              }
          }
      }


