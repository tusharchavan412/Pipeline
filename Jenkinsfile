pipeline{
    agent{
        label {
            label "Slave-1"
            
        }
    }
    stages{
        stage("install httpd"){
            steps{
                sh '''
            sudo yum install httpd -y
            sudo systemctl start http
            '''
            }

        }
         stage("deploy httpd"){
            steps{
                sudo chmod -R 777 /var/www/html
                echo "This is Branch -3 Test web appliation" > /var/www/html/index.html
            }
         }   

     }
  }
