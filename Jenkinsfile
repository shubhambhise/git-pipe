pipeline {
           agent {
		           label {
				   label "built-in"
				   customWorkspace '/mnt/test'
				   }
		   }
          stages {
		           stage ('slave') {
				   agent {
				          label {
						       label '172.31.38.10'	
                              customWorkspace '/mnt/project'							   
						  }
				    }
				          steps {
						  
						  sh "sudo yum install httpd -y"
						  
						  sh "sudo service httpd start"
						  sh "chkconfig httpd on"
						  sh "sudo chmod -R 777 /var/www/html"
						  sh "sudo git clone https://github.com/shubhambhise/git-pipe.git -b master"
						  sh "sudo cp -r /mnt/project/git-pipe/index.html /var/www/html/index.html"
						  
			}
				   }
		  
		  }
}
