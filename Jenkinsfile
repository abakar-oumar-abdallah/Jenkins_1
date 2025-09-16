pipeline {
    agent any

    stages {
        stage ('build') {
            steps {
                echo 'Etape de construction en cours ...'
            // Ici, vous pouvez ajouter les commandes pour compiler votre projet
            // Par exemple : npm run build
                echo "Exécution du build ${env.BUILD_ID} sur ${env.JENKINS_URL}"
            }
        }

        stage ('tests') {
            steps {
                echo 'Etape de test en cours ...'
                // Ici, vous pouvez ajouter les commandes pour tester votre projet
                // Par exemple : npm test
            }
        }

        stage ('deploiement') {
            steps {
                echo 'Etape de déploiement en cours ...'
                // Ici, vous pouvez ajouter les commandes pour déployer votre projet
                // Par exemple : sh 'make deploy'
            }
        }
        
    }
}