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
				steps {
					sh '''
						echo "Step Second"
						echo "Updating Second Stage"
						echo "${EXECUTE}"
					'''
				}
			} 

			stage('Third') {
				steps {
					sh '''
						echo "Step Third"
					'''
				}
			}
		}
}



