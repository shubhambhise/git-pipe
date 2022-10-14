pipeline {
           agent {
		           label {
				   label "built-in"
				   }
		   }
          stages {
		           stage ('slave') {
				   agent {
				          label {
						       label '172.31.38.10'						  
						  }
				    }
				          steps {
						  sh "sudo yum install git -y"
						  sh "sudo yum install httpd -y"
						  
						  sh "sudo service start"
						  sh "chkconfig httpd on"
						  sh "sudo git clone https://github.com/shubhambhise/git-pipe.git -b master"
						  sh "sudo cp -r /mnt/project/git-pipe/index.html /var/www/html/index.html"
						  sh "sudo chmod -R 777 /var/www/html"
			}
				   }
		  
		  }
}
