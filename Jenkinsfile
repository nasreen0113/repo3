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
   stage('step1'){
  sshPut remote: remote, from: 'shaik01.sh', into: '/home/opc'
 }
  stage('step2'){
sshScript remote: remote, script: "shaik01.sh"
 }
  stage('step2'){
 sshCommand remote: remote, command: "pwd"
 }
  stage('step2'){
 sshRemove remote: remote, path: "/home/opc"
 }
}
