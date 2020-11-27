pipeline {
    agent any

    stages {
        
        stage('Compile') {
			steps {
				dir('C:\\devops\\unidad3\\sesion3') {
					bat 'start mvnw.cmd clean compile -e'
				}
			}
		}
        stage('Unit') {    
            	steps {
				dir('C:\\devops\\unidad3\\sesion3') {
					bat 'start mvnw.cmd clean test -e'
				}
			}
        }
        stage('Jar') {
            	steps {
				dir('C:\\devops\\unidad3\\sesion3') {
					bat 'start mvnw.cmd clean package -e'
				}
			}           
        }   
        stage('Run') {    
            	steps {
				dir('C:\\devops\\unidad3\\sesion3') {
					bat 'start mvnw.cmd spring-boot:run'
				}
			}
        }
        stage('Test') {    
           	steps {
				    sleep 10
					bat 'curl http://localhost:8080/rest/mscovid/estadoMundial'
			}
        }
    }
}