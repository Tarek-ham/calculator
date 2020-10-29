pipeline {
	agent any
	stages {
		stage("Compile") {
			steps {
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

