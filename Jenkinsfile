pipeline {
	agent any
	stages {
		stage("Compile") {
			steps {
				sh "source /etc/profile.d/gradle.sh"
				sh "gradle -v"
				sh "./gradlew compileJava"
			}
		}
		stage("Unit test") {
			steps {
				sh "./gradlew test"
			}
		}
	}
}

