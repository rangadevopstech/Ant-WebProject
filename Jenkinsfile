#! groovy
node{
 stage('Source'){
     git 'https://github.com/devopstrainingblr/Ant-WebProject.git'
  
      /* sh 'printenv' */
   /* sh 'env' */
    sh 'echo branch name is:  $env.BRANCH_NAME' 
    sh 'echo git commit is:  $env.GIT_COMMIT'
    sh 'echo Build URL  is:  $env.BUILD_URL'
    sh 'echo JOB_URL  is: $env.JOB_URL'
 }
 
 stage('Build'){
    /* bat "ant -f build-mt.xml" */ /*For windows machines*/
    sh "ant -f build-mt.xml" 
 }
 stage('Send Email'){
     mail bcc: 'mithunreddytechnologies@gmail.com', body: 'Build is done', cc: '', from: '', replyTo: '', subject: 'Build Status', to: 'devopstrainingblr@gmail.com'
 }
 /*stage('Archive'){
  archiveArtifacts '/Users/bhaskarreddyl/.jenkins/workspace/Pipeline-Project-Ant-Web/dist/SampleAntProject.war'
 }*/
}
