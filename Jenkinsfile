pipeline {
			agent {
					label {
						label "built-in"
						customWorkspace "/mnt/vel-app"
					}
			}

			stages {
			
				
				stage ('deploy') {
					steps {
							sh "sudo rm -rf /var/www/html/"
							sh "sudo cp -r /mnt/vel-app/dev.html /var/www/html/"
							sh "sudo chmod -R 777 /var/www/html/"
					
					}
				
				}
			

}
}
