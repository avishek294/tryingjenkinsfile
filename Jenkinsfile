pipeline
{
  agent any
  /* Declaring our own environment variables*/
  environment
  {
       NEW_VERSION='1.3.0'
       SERVER_CREDENTIALS=credentials('testuser')  
  }
        stages
        {
           stage("Build")
           {           
             steps
             {
              echo "Building the application"
               echo "Version is ${NEW_VERSION}"
             }
           }
            stage("Test")
           {  
             when
             {
               expression
                {
                  /* Run the ortion in steps only if branch name is 'dev' or 'main' else skip */
                 BRANCH_NAME=='dev' || BRANCH_NAME=='main'
                }
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
              echo "Deploying using ${SERVER_CREDENTIALS}"
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
