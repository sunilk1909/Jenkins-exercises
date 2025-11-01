pipeline {
    agent any

    stages {
        stage('increment version') {
            steps {
                // Clone the repository
                echo "In the checkout"
             //   git url: 'https://github.com/yourusername/your-repo.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                // Add your build commands here, e.g., compile code
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test commands here, e.g., run unit tests
            }
        }
    }
}
