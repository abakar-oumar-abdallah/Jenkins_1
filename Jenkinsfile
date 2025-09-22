// pipeline {
//     agent any

//     triggers {
//         pollSCM('* * * * *')
//     }

//     stages {
//         stage ('Build et Tests') {
//             steps {
//                 echo 'Build et Tests'
//             // Ici, vous pouvez ajouter les commandes pour compiler votre projet
//             // Par exemple : npm run build
        
//             }
//         }

//         stage ('Deploiement en Production') {
            
//             input {
//                 message "Voulez-vous déployer en production ?"
//                 ok "Oui, déployons."
//                 submitter "admin, devops"
//                 parameters {
//                     string(name: 'VERSION', defaultValue: 'latest', description: 'Quelle version souhaitez-vous déployer ?')
//                 }
//             }

//             steps {
//                 echo "Déploiement de la version ${VERSION} en production."
//                 // Ici, vous pouvez ajouter les commandes pour tester votre projet
//                 // Par exemple : npm test
//             }
//         }

//         // stage ('deploiement') {
//         //     steps {
//         //         echo 'Etape de déploiement en cours ...'
//         //         // Ici, vous pouvez ajouter les commandes pour déployer votre projet
//         //         // Par exemple : sh 'make deploy'
//         //     }
//         // }
        
//     }
// }

pipeline {

    agent any 

    parameters {
        string(name: "PERSONNE", defaultValue: "M. Jenkins", description: "A qui devrais-je dire bonjour ?")
        text(name: "BIOGRAPHIE", defaultValue: "", description: "Entrez des informations")
        booleanParam(name: "TOGGLE", defaultValue: "true", description: "Activez cette valeur")
        choice(name: "CHOIX", choices: ["Un", "Deux", "Trois", "Quatre", "Cinq"], description: "Veuillez choisir")
        password(name: "MOT_DE_PASSE", defaultValue: "Abakar1998.", description: "Entrez un mot de passe")
    }

    stages {

        stage("Build") {
            steps {
                echo "Bonjour: ${PERSONNE}"
                echo "Biographie: ${BIOGRAPHIE}"
                echo "Toggle: ${TOGGLE}"
                echo "Choix: ${CHOIX}"
                echo 'Mot de passe: ${MOT_DE_PASSE}'
                echo "Le build est en cours ..."
            }
        }

        stage("Tests") {
            steps {
                echo "Le test est en cours ..."
            }
        }

        stage("Deploiment") {
            options {
                timestamp(time: 1, unit: "HOURS")
            }
            steps {
                echo "Le déployement est en cours ..."
            }
        }

    }

}