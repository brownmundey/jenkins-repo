pipeline {
    agent {
		label {
			label "slave-1"
			customWorkspace "/mnt/build-tool/apache-maven-3.9.0"/bin
		}
	}

    stages {
        stage ('Compile Stage') {

            steps {
                
                    sh 'sudo mvn compile'
                }
            
        }

        stage ('Testing Stage') {

            steps {
                
                    sh 'sudo mvn test'
                }
            
        }


        stage ('Install Stage') {
            steps {
                
                    sh 'sudo mvn install'
                }
            
        }
        
        stage ('Echo Branch') {

            steps {
                
                    echo "This is master branch"
                }
            
        }
    }
}
