#!groovy

node('master') {

try {
   stage('Checkout'){
  
     checkout scm
      sh''' commit_id=$(git rev-parse HEAD | cut -c1-8)
              echo $commit_id
              '''
      
      		  /*sh''' commit_id=$(git rev-list origin/demo -1 demo | cut -c1-8)
              echo $commit_id*/
              ''' 
          }
           stage('build'){
  
      sh 'echo $commit_id '
              }
  
}

catch (err) {
    currentBuild.result = "FAILURE"
    throw err
 }

}


