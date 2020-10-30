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
		stage("Code coverage") {
			steps {
				sh "./gradlew jacocoTestReport"
				sh "./gradlew jacocoTestCoverageVerification"
			}
		}

	}
}

