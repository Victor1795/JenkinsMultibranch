pipeline {
    agent any
        stages {
            stage('First') {
	        steps {
	   	    script {
		        env.EXECUTE="True"
		    }
		}
                steps {
                    sh "echo Step One"
		    }
		}
            stage('Second') {
	        when { environment name: 'Execute', value: 'True'}
		steps {
	   	    script {
	                echo "Updating Second Stage"
		    }
		}
		steps {
		    sh "echo Step Two"
		    }
		} 
	    stage('Third') {
	        steps {
		    sh "echo Step Three"
		    }
		}
	}
}
