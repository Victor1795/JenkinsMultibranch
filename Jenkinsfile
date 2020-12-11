pipeline {
    agent any
        stages {
            stage("First") {
	        steps {
	   	    script {
		        env.EXECUTE="True"
		    }
		}
                steps {
                    sh "echo Step One"
		    }
		}
            stage("Second") {
	        when {
	            environment name: 'EXECUTE', value: 'True'
		}
		steps {
	   	    sh {
	                "echo Updating Second Stage"
		    }
		}
		steps {
		    sh "echo Step Two"
		    }
		} 
	    stage("Third") {
	        steps {
		    sh "echo Step Three"
		    }
		}
	}
}
