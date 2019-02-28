node ('master'){
  stage('check-out'){
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/kunalkumar229/2048.git']]])
    
    }
  stage('list'){
   sh 'docker build -t twenty48 .'
    sh 'docker images'
    sh 'docker rmi twenty48'
    sh 'docker images'
   
  }
}
