pipeline{
   agent any
   stages{
      stage('copy files to ansible'){
         steps{
            script{
                echo"copy all the files to the ansible machine"
                sshagent(['ansible-server']) {
                   sh "scp -rp -i -o StrictHostKeyChecking=no /home/Mohammed/jenkins/ Mohammed@10.0.0.9:/home/Mohammed/ansible/" 
                   withCredentials([ sshUserPrivateKey(credentialsId: 'test', keyFileVariable: 'keyfile', usernameVariable: 'user')])
                   sh "scp ${keyfile} Mohammed@10.0.0.9:~/ssh-key.pem"
                    
                }
                  
            }   

         }

      } 
      
   }

}