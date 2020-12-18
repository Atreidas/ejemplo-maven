pipeline {
	agent any
	stages {
		stage('Build') {
			steps {
				dir("C:/Users/eduha/OneDrive/Cursos/CORFO/Diplomado especialista DevOps/Unidad III/Sesion 4/Taller S4 M3 Tu primer pipeline/ejemplo-maven") {
					sh './mvnw.cmd clean compile -e'
				}
			}
		}
		stage('Test') {
			steps {
				dir("C:/Users/eduha/OneDrive/Cursos/CORFO/Diplomado especialista DevOps/Unidad III/Sesion 4/Taller S4 M3 Tu primer pipeline/ejemplo-maven") {
					sh './mvnw.cmd clean test -e'
				}
			}
		}
		stage('Deploy') {
			steps {
				dir("C:/Users/eduha/OneDrive/Cursos/CORFO/Diplomado especialista DevOps/Unidad III/Sesion 4/Taller S4 M3 Tu primer pipeline/ejemplo-maven") {
					sh './mvnw.cmd clean package -e'
				}
			}
		}
		stage('Run') {
			steps {
				dir("C:/Users/eduha/OneDrive/Cursos/CORFO/Diplomado especialista DevOps/Unidad III/Sesion 4/Taller S4 M3 Tu primer pipeline/ejemplo-maven") {
					sh './mvnw.cmd spring-boot:run'
				}
			}
		}
	}
}