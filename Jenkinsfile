pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages {
        stage ('Build et Tests') {
            steps {
                echo 'Build et Tests'
            // Ici, vous pouvez ajouter les commandes pour compiler votre projet
            // Par exemple : npm run build
        
            }
        }

        stage ('Deploiement en Production') {
            
            input {
                message "Voulez-vous déployer en production ?"
                ok "Oui, déployons."
                submitter "admin, devops"
                parameters {
                    string(name: 'VERSION', defaultValue: 'latest', description: 'Quelle version souhaitez-vous déployer ?')
                }
            }

            steps {
                echo "Déploiement de la version ${VERSION} en production."
                // Ici, vous pouvez ajouter les commandes pour tester votre projet
                // Par exemple : npm test
            }
        }

        // stage ('deploiement') {
        //     steps {
        //         echo 'Etape de déploiement en cours ...'
        //         // Ici, vous pouvez ajouter les commandes pour déployer votre projet
        //         // Par exemple : sh 'make deploy'
        //     }
        // }
        
    }
}