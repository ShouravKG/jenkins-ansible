pipeline{
 agent any
 stages{
 stage('code checkout'){
  steps{
       git branch: 'main', credentialsId: 'ansible1', url: 'https://github.com/ShouravKG/jenkins-ansible.git'
       }
 }
 stage('Execute Ansible'){
  steps{
     ansiblePlaybook credentialsId: 'paru', disableHostKeyChecking: true, inventory: 'dhost.yml', playbook: 'apache.yml'  
      }
    }
}
}
