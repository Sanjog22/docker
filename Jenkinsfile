pipeline {
		agent {
			label { 
				label 'built-in'
				customWorkspace '/mnt/project/assignment1/22Q2'
			}
		}
		stages {
			 stage('kill') {
				steps {
					sh "docker stop 22Q2"
					sh "docker rm 22Q2"
					sh "docker rmi httpd"
				}
			} 
			stage('docker-22Q2') {
				steps {
					sh "docker run --name 22Q2 -itdp 80:80 httpd"
					sh "chmod -R 777 /mnt/project/assignment1/22Q2/index.html"
					sh "cd /mnt/project/assignment1/22Q2 && docker cp index.html 22Q2:/usr/local/apache2/htdocs/"
				}
				
			
			}
		
		}
		
}
