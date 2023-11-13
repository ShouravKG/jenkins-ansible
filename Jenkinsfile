pipeline{
 agent any
 stages{
 stage('code checkout'){
  steps{
       git branch: 'main', credentialsId: 'paru', url: 'https://github.com/ShouravKG/jenkins-ansible.git'
       }
 }
 stage('Execute Ansible'){
  steps{
     ansiblePlaybook credentialsId: 'skghosh', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dhost.inv', playbook: 'apache.yml', vaultTmpPath: ''  
      }
    }
}
}
