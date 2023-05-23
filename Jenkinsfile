node{
  def remote = [:]
  remote.name = 'oraclevm'
  remote.host = '152.67.160.182'
  remote.user = 'opc'
  remote.password = 'Muzammil073#'
  remote.allowAnyHosts = true
    stage('checkout') {
           checkout scm
  }  
  stage('Remote SSH') {
   // writeFile file: 'jenkinsfile.sh', text: 'ls -lrt'
   // sshScript remote: remote, script: "jenkinsfile.sh"
    sshCommand remote : remote, command: "pwd"
      sshCommand remote : remote, command: "cd /home"
    sshCommand remote : remote, command: "pwd"
      sshCommand remote : remote, command: "ls -lrt"
  }     
  
   stage('Remote SSH 2') {
    writeFile file: 'jenkinsfile.sh', text: 'ls -lrt'
    sshScript remote: remote, script: "jenkinsfile.sh"
  }
}
  
  stage('Remote SSH 3') {
   sshScript remote: remote, script: "./micro/args.sh"
  }  
        }
