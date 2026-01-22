pipeline{
agent any

tools{
maven 'mymaven'
}

stages{
    

stage('Build Code')
{
  steps{
        git 'https://github.com/Varad5005/Jenkinsfile-Demo-pipleineCode.git'
        sh 'mvn package'
        script{
          timeout(time: 10,unit: 'MINUTES'){
          input(id: 'DeplpoyCode',message: 'Continue Deploy stage',ok: 'Deploy')
       }
    }
 
  }

}

stage('Deploy Code')
{

 steps{
        echo "Deployment Completed"
 }
}

}
}
