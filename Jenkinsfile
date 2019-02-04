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
}
