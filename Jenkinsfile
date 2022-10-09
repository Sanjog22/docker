pipeline {
		agent {
			label { 
				label 'built-in'
				customWorkspace '/mnt/project/assignment1/22Q3'
			}
		}
		Stages {
			/* stage('kill') {
				steps {
					sh "docker kill 22Q3"
					sh "docker rm 22Q3"
					sh "docker rmi httpd"
				}
			} */
			Stage('docker-22Q3') {
				Steps {
					sh "docker run --name 22Q3 -itdp 90:80 httpd"
					sh "chmod -R 777 /mnt/project/assignment1/22Q3/index.html"
					sh "cd /mnt/project/assignment1/22Q3 && docker cp index.html 22Q3:/usr/local/apache2/htdocs/"
				}
				
			
			}
		
		}
		
}
