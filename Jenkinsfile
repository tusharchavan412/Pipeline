
pipeline{
    agent{
        label {
            label "Slave-3"
            
        }
    }
    stages{
        stage("install httpd"){
            steps{
                sh '''
            sudo yum install httpd -y
            sudo systemctl start httpd
            '''
            }

        }
         stage("deploy httpd"){
            steps{
                sh '''
                sudo chmod -R 777 /var/www/html
                echo "This is Branch -3 Test web appliation" > /var/www/html/index.html
                '''
            }
         }            


        
           
            
    }
      
        
}
