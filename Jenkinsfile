node{
  stage('SCM Checkout'){
  git 'https://github.com/shrinathdm/Mavenapp'
  }
  stage('Compile-Package'){
  sh 'mvn package'
  }
}
