pipeline
{
      agent any
      stages
      {
            stage('Build Application')
            {
                  steps
                  {
                         bat 'mvn clean package'
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
