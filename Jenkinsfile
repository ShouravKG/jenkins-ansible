pipeline{
 agent any
 stages{
 stage('code checkout'){
  steps{
       git branch: 'main', credentialsId: 'git credentials', url: 'https://github.com/ShouravKG/jenkins-ansible.git'
       }
 }
 stage('Execute Ansible'){
  steps{
     ansiblePlaybook credentialsId: 'ansible1', disableHostKeyChecking: true, inventory: 'dhost.inv', playbook: 'apache.yml'  
      }
    }
}
}
