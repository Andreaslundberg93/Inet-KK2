pipeline {
    agent { label "built-in" }
    stages {
        stage("Running tests") {
            steps { 
                
                bat "java -m unittest test_inet.py" 
                echo "Testing" 
            }
                 
        } 
    } 
    post("Cleanup") {
        always { 
            cleanWs() 
            echo "Cleaning up" 
            } 
        } 
    }