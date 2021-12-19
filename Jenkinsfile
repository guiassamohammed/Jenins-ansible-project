pipeline{
   agent any
   stages{
      stage('copy files to ansible'){
         steps{
            script{
                echo"copy all the files to the ansible machine"
                sshagent(['ansible-server']) {
                   sh "su - "
                   sh "scp -o StrictHostKeyChecking=no /home/Mohammed/jenkins/* root@10.0.0.9:/root" 
                  
   
                }
                  
            }   

         }

      } 
      
   }

}