---
title: Utilisation du Kit de certification des applications Windows
description: pour que votre application de bureau soit la meilleure chance d’obtenir une certification, validez-la et testez-la sur votre ordinateur avant de la soumettre à des fins de certification et de référencement dans le magasin de Windows.
ms.assetid: 8B460B84-0997-4987-9B66-90F9C6D88D83
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8692e87f8bd152b730129c0d8684bc7ec2ca91964ecd6c25e98eb3db3e0fce44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118708747"
---
# <a name="using-the-windows-app-certification-kit"></a>Utilisation du Kit de certification des applications Windows

pour que votre application de bureau soit la meilleure chance d’obtenir une certification, validez-la et testez-la sur votre ordinateur avant de la soumettre à des fins de certification et de référencement dans le magasin de Windows. pour certifier votre application, vous devez installer et exécuter le [Kit de Certification des applications Windows](/previous-versions//mt637081(v=vs.85)). pour plus d’informations sur les tests spécifiques au sein du kit, reportez-vous à [Windows tests du kit de Certification des applications](windows-app-certification-kit-tests.md).

Pour une vue d’ensemble du processus de certification, et où l’utilisation de cet outil s’adapte à, consultez [certifier votre application de bureau](windows-certification-portal.md).

la version actuelle de Windows ACK est disponible en 14 langues (tchèque, anglais, français, allemand, italien, japonais, coréen, polonais, portugais (brésil), russe, chinois simplifié, espagnol, chinois traditionnel et turc).

## <a name="prerequisites"></a>Prérequis

avant d’installer le Windows ACK, vous devez installer et exécuter le système d’exploitation.

1. Installez et exécutez le système d’exploitation pour lequel vous développez des applications.

-   si vous développez des applications pour Windows 7, vous pouvez installer et exécuter Windows 7, Windows 8 ou Windows 8.1.
-   si vous développez une application de bureau Windows 8 ou une application Windows 8 desktop device, vous pouvez installer et exécuter Windows 8 ou Windows 8.1.
-   si vous développez une application de bureau Windows 8.1 ou une application Windows 8 desktop device, installez Windows 8.1.

2. installez le [kit de Certification des applications Windows 3,3](/previous-versions//mt637081(v=vs.85)), qui est inclus dans le kit de développement logiciel (SDK) Windows pour Windows 8.1.

**Remarque :** lorsque vous installez Windows kit de Certification des applications 3,3 ou version ultérieure sur votre PC, vous remplacez toute version précédemment installée du kit.

## <a name="instructions-to-run-windows-app-certification-kit-33"></a>Instructions pour exécuter Windows Kit de Certification des applications 3,3

**valider votre application de bureau à l’aide du Kit de Certification des applications Windows 3,3 de manière interactive**

1.  dans le menu Démarrer, recherchez Windows App Cert Kit.
2.  dans le Windows Kit de Certification des applications, cliquez sur la catégorie de validation de test que vous souhaitez exécuter. Si vous validez une application de bureau, sélectionnez **valider l’application de bureau**.
3.  Dans l’écran suivant, accédez au fichier d’installation de l’application de bureau que vous souhaitez valider.
    -   **Remarque :** Vous pouvez utiliser les [étapes](#commandlinesteps) de la ligne de commande pour inclure des options ou un commutateur d’installation, si nécessaire.
4.  Indiquez le type d’utilisation de l’application, puis cliquez sur **suivant**. le Kit de Certification des applications Windows démarre l’installation de l’application de bureau à l’aide des fichiers d’installation afin de pouvoir valider l’installation.
5.  Si vous êtes invité à redémarrer le système pour terminer l’installation, choisissez **non**. Si votre application a besoin d’installer plusieurs composants ou des dépendances externes, sélectionnez avec soin le nom de votre application. le nom que vous choisissez ici est le nom que votre application reçoit si elle est répertoriée dans le magasin de Windows. Une fois la validation terminée, enregistrez le rapport avec le nom que vous avez donné à votre application à l’étape 6. le Kit de Certification des applications Windows crée un fichier de rapport XML et l’enregistre.
6.  Accédez au dossier dans lequel vous avez enregistré le rapport et ouvrez-le pour afficher les résultats du test. Si votre test a échoué et que vous êtes éligible à une renonciation, les informations que vous devez envoyer sont répertoriées ici. Vous devez soumettre une description détaillée de chaque demande de dérogation possible.

**valider votre application de bureau Windows à l’aide du Kit de Certification des applications Windows 3,3 à partir d’une ligne de commande**

1.  Accédez au dossier dans lequel vous avez enregistré le rapport et ouvrez-le pour afficher les résultats du test. Les tests ayant échoué avec une demande de renonciation possible sont répertoriés ici. Vous devez soumettre une description détaillée de chaque demande de dérogation possible.
2.  dans le dossier qui contient le Kit de Certification des applications Windows, entrez ces commandes dans l’ordre suivant :

    -   <span id="commandLineSteps"></span><span id="commandlinesteps"></span><span id="COMMANDLINESTEPS"></span>`appcert.exe reset`
    -   `appcert test -apptype desktop -setuppath d:\cdrom\setup.exe  -appusage peruser -reportoutputpath [report file name]`

    où : `[report file name]` est le nom de fichier complet du fichier XML que le kit va créer pour contenir le rapport de test.

3.  Une fois le test terminé, ouvrez le fichier de rapport nommé \[ nom \] du fichier de rapport et affichez les résultats des tests.

    **Remarque :** pour plus d’informations sur la ligne de commande du Kit de Certification de l’application Windows, entrez la commande appcert.exe/ ?

    le Kit de Certification des applications Windows doit être exécuté dans le contexte d’une session utilisateur active, mais vous ne pouvez pas lancer des applications dans une session non interactive. La façon dont le kit gère les jetons pour l’exécution des tests avec ou sans privilèges d’administration dépend également du contexte de cette session utilisateur. Le kit peut être exécuté à partir d’un service, mais le service doit être en mesure de générer le processus de kit dans une session utilisateur active.

**utiliser le Kit de Certification des applications Windows pour valider vos applications Windows 7**

-   le kit de Certification des applications Windows a remplacé le kit de Logo Windows Software. si vous souhaitez obtenir le logo Windows 7 pour votre application, utilisez le Kit de Certification des applications Windows pour le test et le rapport de validation. le kit peut détecter le système d’exploitation sur lequel il s’exécute et se lance automatiquement pour les applications Windows 7. suivez le même processus pour valider les applications Windows 7.

**Soumettre pour certification**

-   Une fois votre application validée, vous êtes prêt à la soumettre pour certification [par le biais du processus d’envoi du portail](https://www.microsoft.com/?ref=go).

## <a name="reference-documents"></a>Documents de référence

-   [conditions de Certification pour les applications de bureau Windows](/windows/desktop/win_cert/certification-requirements-for-windows-desktop-apps)
-   [Livre blanc sur la certification des applications](https://www.microsoft.com/download/details.aspx?id=27414)
-   [Windows Stocker l’intégration pour les applications de bureau](/previous-versions//dn322034(v=vs.85))
-   [conditions de certification des applications de bureau Windows 7](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)

## <a name="windows-app-certification-kit-tests"></a>Tests du Kit de certification des applications Windows

nous avons modifié le kit pour faciliter l’utilisation des tests de l' [Windows ACK](windows-app-certification-kit-tests.md) . Le kit dispose maintenant des éléments suivants :

-   Une nouvelle interface utilisateur simplifiée
-   Amélioration du test multi-utilisateur, qui ne nécessite plus la configuration d’un deuxième compte d’utilisateur

 

 