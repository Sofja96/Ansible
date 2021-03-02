
pipeline {


    agent { label 'slave' }
    stages {
        stage('Stage 1') {
            steps {
                sh 'docker ps'
                     catchError {
          sh " psql -h 172.20.0.1 -p 5432 -U postgres -c 'SELECT * FROM users'"
        }
      }
      post {
        success {
          echo 'Build stage successful'
	   script{
             ansiColor('xterm') {
              ansiblePlaybook(
            colorized: true,
	    disableHostKeyChecking: true,
            //installation: 'ansible',
            inventory: '/home/user-admin/Ansible/hosts',
            credentialsId: 'private_key',
            playbook: "/home/user-admin/Ansible/config.yml",
            //extras: ''
	)
    }
}
        }
        failure {
          echo 'Compile stage failed'


         // sh "ansible-playbook -i /home/user-admin/Ansible/hosts /home/user-admin/Ansible/config.yml -vD"
	}
      }
	}
    }
}
	
