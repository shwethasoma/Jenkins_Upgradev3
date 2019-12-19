pipeline
{
      agent any
      stages
      {
            stage('Build Application')
            {
                  steps
                  {
                         bat 'mvn -f java-tomcat-sample/pom.xml clean package'
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
