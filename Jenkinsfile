pipeline{
    
    agent any
    tools { maven "maven_3_6_3" }
    stages{
        
        stage("checkout"){
            steps {
                git branch : "main", url : "https://github.com/MaherKarzoun/SpringPetClinic.git"
            }
        }
        
        stage("build"){
            steps{
                sh "mvn compile -DskipTests"
            }
        }
        
        stage("test"){
            steps{
                echo "skipping tests"
            }
        }
        
        stage("package"){
            steps{
                sh "mvn package -DskipTests"
            }
        }
        
        stage("deploy"){
            steps{
                sh "java -jar /Users/maherkarzoun/.jenkins/workspace/PET-CLINIC-DECLARATIVE-PIPELINE/target/*.jar"
            }
        }
    }
}
