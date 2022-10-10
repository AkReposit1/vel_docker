pipeline{
        agent{
                label{
                        label 'Slave1'
                        customWorkspace '/mnt/projects/22Q2'
                }
        }


        stages{
                stage('create volume and bind container'){
                    steps{
                        sh"sudo docker system prune -a -f"
                        sh"sudo docker volume create 22Q2volume"
                        sh"sudo cp -r /mnt/projects/22Q2/index.html /var/lib/docker/volumes/22Q2volume/_data"
                        sh"sudo docker run --name container2 -itdp 90:80 -v 22Q2volume:/usr/local/apache2/htdocs httpd"
                    }
                }
        }
}
