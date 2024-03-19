library identifier: 'shared_lib_pipeline@main',
      retriever: modernSCM([$class: 'GitSCMSource', remote: 'https://github.com/bhardwaj-abhinav/shared_lib_pipeline.git'])

pipeline{
      agent any 

      stages{
            stage("Audit Tools"){
                  steps{
                        auditTools()
                  }
            }
            
            stage("compile"){
                  steps{
                        sh 'javac Test.java'
                  }
            }

            stage("run"){
                  steps{
                        sh "java Test"
                  }
            }
      }
}
