pipeline {
  agent any

  stages {
    stage ('Deploy Website') {
      steps {
        sh '''
        scp -i day1-key.pem index.html ec2-user@15.207.249.198:/home/ec2-user/
        ssh -i day-key.pem ec2-user@15.207.249.198 "sudo mv /home/ec2-user/index.html /usr/share/nginx/html/index.html"
        '''
      }
    }
  }
}
