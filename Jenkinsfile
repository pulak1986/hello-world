node{
  stage('SCM Checkout')
  {
    git 'https://github.com/pulak1986/hello-world.git'
  }
  stage('Compile Package')
  {
   sh 'mvn package'
  }
}
