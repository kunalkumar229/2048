node ('master'){
 
  stage('check-out'){
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/kunalkumar229/2048.git']]])
    
    }
  stage('docker'){
   //sh 'docker build -t twenty48 .'
    sh 'docker images'
   
  }
   stage('run'){
     
   //sh 'docker run -d -p 8087:80 twenty48'
     //sh 'docker stop jolly_pare'
     sh 'docker rmi twenty48'
     sh 'docker images'
     //sh 'docker ps'
   }
  
}
