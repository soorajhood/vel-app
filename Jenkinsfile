pipeline {
			agent {
					label {
						label "slave-1"
						customWorkspace "/mnt/vel-app"
					}
			}

			stages {
				stage ('install-httpd') {
					steps {
						sh "sudo yum install httpd -y"
				}
				}
			
				stage ('start-httpd') {
					steps {
						sh "sudo service httpd start"
				}
				}
				
				stage ('deploy') {
					steps {
							sh "sudo cp -r /mnt/vel-app/index.html /var/www/html/"
							sh "sudo cp -r /mnt/vel-app/dev.html /var/www/html/"
							sh "sudo chmod -R 777 /var/www/html/"
					
					}
				
				}
			

}
}
