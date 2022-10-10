pipeline{
        agent{
                label{
                        label 'Slave1'
                        customWorkspace '/mnt/projects/22Q3'
                }
        }


        stages{
                stage('create volume and bind container'){
                    steps{
                        sh"sudo docker system prune -a -f"
                        sh"sudo docker volume create 22Q3volume"
                        sh"sudo cp -r /mnt/projects/22Q3/index.html /var/lib/docker/volumes/22Q3volume/_data"
                        sh"sudo docker run --name container3 -itdp 8080:80 -v 22Q3volume:/usr/local/apache2/htdocs httpd"
                    }
                }
        }
}
