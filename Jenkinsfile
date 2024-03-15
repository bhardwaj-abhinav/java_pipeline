library identifier: 'shared_lib_pipeline@main',
      retriever: modernSCM([$class: 'GitSCMSource', remote: 'https://github.com/bhardwaj-abhinav/shared_lib_pipeline.git'])

pipeline{
      agent any 

      stages{
            stages("Audit Tools"){
                  steps{
                        auditTools()
                  }
            }
            
            stage("compile"){
                  steps{
                        bat 'javac Test.java'
                  }
            }

            stage("run"){
                  steps{
                        bat "java Test"
                  }
            }
      }
}
