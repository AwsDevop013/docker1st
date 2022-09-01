pipeline{
	agent{
		label{label 'built-in'
		customWorkspace '/root/ansible/'
		}
		}
		stages{
		
		stage('dev-branch'){
		steps{ 
		sh "rm -rf dev"
		dir('/root/ansible/dev/'){
		sh "git clone https://github.com/AwsDevop013/docker1st.git -b dev "
		}
		}
		}
		stage('qa-branch'){
		steps{ 
		sh "rm -rf qa"
		dir('/root/ansible/qa/'){
		sh "git clone https://github.com/AwsDevop013/docker1st.git -b qa "
		}
		}
		}
		stage('ansible-playbook'){
		steps{ 
		sh "ansible-playbook /mnt/httpd.yaml"
		
		}
		}
		
	}
}
