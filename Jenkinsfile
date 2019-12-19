pipeline
{
      agent any
      stages
      {
            stage('Build Application')
            {
                  steps
                  {
                        sh 'mvn clean package'
                  }
                  post
                  {
                        success
                        {
                              echo "Now archiving the artifact"
                              archiveArtifacts artifacts:'**/*.war'
                        }
                  }
            }
      }
}
