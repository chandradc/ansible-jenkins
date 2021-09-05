pipeline{
    agent any
    stages{
        stage('Checkout'){
            steps{
               git 'https://github.com/chandradc/ansible-jenkins.git' 
            }
        }
            stage('Run playbook')
            {
                steps{
                    
                   ansiblePlaybook credentialsId: 'myansssh', disableHostKeyChecking: true, installation: 'myansible', inventory: 'hosts.ini', playbook: 'install_git.yml'
                }
                    
           }
            
        }
        
    
}
