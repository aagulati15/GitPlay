node {
  stage ('Checkout') 
  {
    // Get the code from the Git repository
    checkout scm
  } 
  
  stage('Git to ISPW Synchronization')
  { 
	gitToIspwIntegration app: 'TXX2', 
	branchMapping:  '''*Play* => DEV1, per-branch''',
	connectionId: 'cw09-47623', 
	credentialsId: 'pinjxa0-tso', 
	gitCredentialsId: 'jaroragit', 
	gitRepoUrl: 'https://github.com/jarora8/GitPlay.git', 
	runtimeConfig: 'tpzp', 
    stream: 'CWEZ',
    ispwConfigPath: 'ispwconfig.yml' 
  }  
  
}