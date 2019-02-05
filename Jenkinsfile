node{
  stage('SCM Checkout'){
  git 'https://github.com/shrinathdm/Mavenapp'
  }
  stage('Test'){
  sh 'mvn test'
   }
   stage('Build'){
   sh 'mvn package'
   }
   stage('send to email'){
   emailext (
      subject: "STARTED: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
      body: """<p>STARTED: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]':</p>
        <p>Check console output at "<a href="${env.BUILD_URL}">${env.JOB_NAME} [${env.BUILD_NUMBER}]</a>"</p>""",
      recipientProviders: [[$class: 'DevelopersRecipientProvider']]
    )
   }
}
