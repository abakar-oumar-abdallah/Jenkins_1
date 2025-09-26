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
//         //         // Par exemple : sh 'make deploy' Important
//         //     }
//         // }
        
//     }
// }


// pipeline {

//     agent none 

//     stages {

//         stage('Build et Test') {
//             agent {label 'build'}
//             steps {
//                 echo "Construire et tester l'application"
//             }
//         }

//         stage('Déploiement séquentiel') {
//             agent {label 'deploy'}
//             stages {
//                 stage('Déploiement Dev') {
//                     steps {
//                         echo "Déploiement dans l'environnement de développement"
//                     }
//                 }

//                 stage('Déploiement Staging') {
//                     steps {
//                         echo "Déploiement en environnement de pré-production"
//                     }
//                 }
//             }
//         }

//     }

// }

pipeline {
    agent any
<<<<<<< HEAD
    
    parameters {
        booleanParam(name: 'RUN_BUILD', defaultValue: true)
    }

=======
>>>>>>> 7b843b925cfb0853bea8b7b565eac4e850c30341
    stages {
        stage('Build et Test') {
            steps {
<<<<<<< HEAD
                echo 'Run Build is true'
=======
                echo "Construire et tester l'application."
            }
        }
        stage('Déploiement parallèle') {
            failFast true
            parallel {
                stage('Déploiement Dev') {
                    steps {
                        echo "Déploiement en environnement de développement."
                    }
                }
                stage('Déploiement Staging') {
                    steps {
                        echo "Déploiement en environnement de préproduction."
                    }
                }
>>>>>>> 7b843b925cfb0853bea8b7b565eac4e850c30341
            }
        }
    }
}