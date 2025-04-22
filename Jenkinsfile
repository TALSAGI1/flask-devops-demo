pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    def imageName = 'my-flask-app' // שנה את שם התמונה לפי הצורך

                    // בניית התמונה
                    sh "docker build -t ${imageName} ."

                    // הצגת תמונות דוקר (לבדיקה)
                    sh "docker images ${imageName}"
                }
            }
        }

        // אפשר להוסיף כאן שלבים כמו הרצת בדיקות, העלאה ל-DockerHub, הפצה וכו'
    }
}
