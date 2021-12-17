pipeline {
	agent any
		stages {
			stage('First') {
				steps {
						
					sh '''
						echo "Step First"
						EXECUTE='true'
					'''
				}
			}


			stage('Second') {
				when {
					environment name: 'EXECUTE', value: 'true'
				}	
				steps {
					sh '''
						echo "Step Second"
						echo "Updating Second Stage"
					'''
				}
			} 

			stage('Third') {
				when {
					environment name: 'EXECUTE', value: 'false'
				}
				steps {
					sh '''
						echo "Step Third"
					'''
				}
			}
		}
}



