pipeline
{
  agent any
        stages
        {
           stage("Build")
           {           
             steps
             {
              echo "Building the application"
             }
           }
            stage("Test")
           {  
             when
             {
               BRANCH_NAME=='dev'
             }
             steps
             {
              echo "Testing the application"
             }
           }
            stage("Deploying")
           {           
             steps
             {
              echo "Deploying the application"
             }
           }
        
        }
    post 
        { 
        always 
          { 
            echo 'I will always say Hello again!'
          }
        }
}
