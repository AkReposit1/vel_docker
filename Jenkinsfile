/*pipeline{
        agent{
                label{
                        label 'Slave1'
                        customWorkspace '/mnt/projects/master'
                }
        }
        
        
        stages{
                stage('docker stop containers'){
                        steps{
                                
                                //sudo docker stop $('docker ps -q')
                                //sudo docker rm $('docker ps -a')
                                sh"sudo docker system prune -a -f"
                                
                        }
                }*/
                
                //multibranch will clone in /mnt/projects/22Q1 /22Q2 /22Q3 
                /*stage('docker start and bind containers'){
                        steps{
                                sh'''
                                    sudo docker run --name container1 -itdp 80:80 -v /mnt/projects/22Q1:/usr/local/apache2/htdocs httpd
                                    sudo docker run --name container2 -itdp 90:80 -v /mnt/projects/22Q2:/usr/local/apache2/htdocs httpd
                                    sudo docker run --name container3 -itdp 8080:80 -v /mnt/projects/22Q3:/usr/local/apache2/htdocs httpd
                                '''
                        }
                }*/ /*
                stage('docker create volume'){
                        steps{
                                sh'''
                                    sudo docker volume create dockervolume
                                    sudo docker volume create dockervolume2
                                    sudo docker volume create dockervolume3
                                    
                                '''
                        }
                }
                stage('copy index.html to docker volumes'){
                        steps{
                                sh'''
                                sudo cp -r /mnt/projects/22Q1/index.html /var/lib/docker/volumes/dockervolume/_data
                                sudo cp -r /mnt/projects/22Q2/index.html /var/lib/docker/volumes/dockervolume2/_data
                                sudo cp -r /mnt/projects/22Q3/index.html /var/lib/docker/volumes/dockervolume3/_data
                                '''
                        }
                }
                stage('docker start containers'){
                        steps{
                                sh'''
                                    sudo docker run --name container1 -itdp 80:80 -v dockervolume:/usr/local/apache2/htdocs httpd
                                    sudo docker run --name container2 -itdp 90:80 -v dockervolume2:/usr/local/apache2/htdocs httpd
                                    sudo docker run --name container3 -itdp 8080:80 -v dockervolume3:/usr/local/apache2/htdocs httpd
                                '''
                        }
                }
        }
}*/
