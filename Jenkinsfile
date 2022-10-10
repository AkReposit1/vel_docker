pipeline{
        agent{
                label{
                        label 'Slave1'
                        customWorkspace '/mnt/projects/'
                }
        }
        
        
        stages{
                stage('create volume and bind container'){
                    steps{
                        sh"sudo docker system prune -a -f"
                        sh"sudo docker volume create 22Q1volume"
                        sh"sudo cp -r /mnt/projects/22Q1/index.html /var/lib/docker/volumes/22Q1volume/_data"
                        sh"sudo docker run --name container1 -itdp 80:80 -v 22Q1volume:/usr/local/apache2/htdocs httpd"
                    }
                }
        }
}


