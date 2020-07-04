node {
  echo "GitHub BranhName ${env.BRANCH_NAME}"
  echo "Jenkins Job Number ${env.BUILD_NUMBER}"
  echo "Jenkins Node Name ${env.NODE_NAME}"
  echo "Jenkins Home ${env.JENKINS_HOME}"
  echo "Jenkins URL ${env.JENKINS_URL}"
  echo "JOB Name ${env.JOB_NAME}"
       def mavenhome = tool name: "maven-3.6.1", type: "maven"
       def mavencmd = "${mavenhome}/bin/mvn clean package"
    stage ("git clone"){
        
        git credentialsId: 'GIT_CREDENTIALS', url: 'https://github.com/jmjyotiranjan2018/radha'
    }
   
   stage ("maven clean build") {
       sh "${mavencmd}"
       def currentResult = currentBuild.result
   }
   
}
