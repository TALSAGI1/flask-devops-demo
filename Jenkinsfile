pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    def imageName = 'my-flask-app' // שנה את שם התמונה לפי הצורך
                    def dockerfilePath = '.' // הנתיב ל-Dockerfile (במקרה זה, בשורש המאגר)

                    // בניית תמונת הדוקר
                    sh "docker build -t ${imageName} -f ${dockerfilePath}"

                    // אופציונלי: בדיקה שהתמונה נוצרה (לצרכי דיבאג)
                    sh "docker images ${imageName}"
                }
            }
        }
        // שלבים נוספים יכולים לבוא כאן, כמו בדיקות יחידה, העלאת התמונה ל-Docker Hub, או פריסה
    }
}