pipeline {
   agent {
	  label "${params.slave_name}"
	}

   stages {
      stage('Clone') {
         steps {
      // Get some code from a GitHub repository
          checkout scm
         }
      }
      stage('Build') {
         steps {
            // Run Maven on a Unix agent.
		 sh "${params.build_cmd}"

            // To run Maven on a Windows agent, use
            // bat "mvn -Dmaven.test.failure.ignore=true clean package"
         }
      }
      
        
   }
}
