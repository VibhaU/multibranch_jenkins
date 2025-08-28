pipeline{
   agent any
   stages{
	stage('clean workspace')
	{
           steps{
              sh ' rm -r *'
	      sh ' rm -r ../../../../www/html/*'
	   }
	}

        stage('git scm clone'){
             
	     steps{
                  
		  sh ' git clone https://github.com/VibhaU/multibranch_jenkins.git -b main'

	     }
 
	}
	stage('deploy'){
              steps{
                sh 'mv multibranch_jenkins/* ../../../../www/html'
	      }
	}
     
   }
  
}
