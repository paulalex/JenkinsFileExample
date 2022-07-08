pipeline {
  agent any

  stages {
    stage("Test Service A") {
      steps {
        echo "Testing Service A"
      }
    }

    stage("Test Service B") {
      steps {
        echo "Testing Service B"
      }
    }

    stage("Test Service C") {
      steps {
        echo "Testing Service C"
      }
    }

    stage("Build Service A") {
      when { changeset "service_a/*" }
      steps {
        echo "Building Service A"
      }
    }

    stage("Build Service B") {
      when { changeset "service_b/*" }
      steps {
        echo "Building Service B"
      }
    }

    stage("Build Service C") {
      when { changeset "service_c/*" }
      steps {
        echo "Building Service C"
      }
    }

    stage("deploy") {
      steps {
        echo "Deploying Application"
      }
    }

    stage("smoke_test") {
      steps {
        echo "Smoke Testing Application"
      }
    }
  }
}