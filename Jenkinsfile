pipeline{
  agent any
  stages {
//          stage('Clone repository'){
 //           steps {
  //            checkout([$class: 'GitSCM',
   //           branches: [[name: '*/main']],
     //         userRemoteConfigs: [[url: 'https://github.com/saicharan1901/PES2UG21CS364_Jenkins.git']]])
       //     }
         // }
    stage('Build'){
        steps {
          build 'PES2UG21CS364-1'
          sh 'g++ sample.cpp -o output'
        }
    }
    stage('Test') {
      steps {
        sh './output'
        }
    }
    stage('Deploy') {
        steps {
            echo 'deploy'
        }
    }
}
post{
  failure{
    error 'Pipeline failed'
  }
}
}
