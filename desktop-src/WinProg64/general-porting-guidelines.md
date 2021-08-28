---
title: Instructions générales sur le portage
description: le portage des applications 32 bits vers les Windows Microsoft 64 bits est plus facile qu’avec les applications 16 bits qui ont été déplacées vers des Windows 32 bits. Toutefois, le déplacement sera plus fluide avec une planification minutieuse. Voici quelques recommandations générales.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- portage d’applications 32 bits vers la programmation Windows Windows 64 bits de 64 bits
- guide de programmation Windows 64 bits 64-bits Windows programmation, indications de portage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a586318ecc6ec8852077052cbcff41bffacff6c35c36d23de4b020ce19f12af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680239"
---
# <a name="general-porting-guidelines"></a>Instructions générales sur le portage

le portage des applications 32 bits vers les Windows Microsoft 64 bits est plus facile qu’avec les applications 16 bits qui ont été déplacées vers des Windows 32 bits. Toutefois, le déplacement sera plus fluide avec une planification minutieuse. Voici quelques recommandations générales.

## <a name="planning"></a>Planification

-   Déterminez l’ampleur de l’effort requis pour le port. Évaluer la quantité de travail impliquée par l’identification des éléments suivants :
    -   Problème 32-code bit. Compilez votre code 32 bits avec le compilateur 64 bits et examinez l’étendue des erreurs et des avertissements.
    -   Composants partagés ou dépendances. Identifiez les composants de votre application qui proviennent d’autres équipes et si ces équipes envisagent de développer des versions 64 bits de leur code.
    -   Code d’héritage ou d’assembly. les applications à base de Windows 16 bits ne s’exécutent pas sur le Windows 64 bits et doivent être réécrites. Bien que le code assembleur x86 s’exécute dans WOW64, vous pouvez réécrire ce code pour tirer parti de la vitesse de l’architecture Intel Itanium.
-   Portage de l’application entière, et pas seulement d’une partie de celle-ci.

    Bien qu’il soit possible de porter des parties d’une application ou de limiter le code à 2G avec/LARGEADDRESSAWARE : NO, cette stratégie offre des gains à long terme pour la douleur à long terme.

    > [!Note]  
    > /LARGEADDRESSAWARE : NO est ignoré pour un binaire ARM64.

     

-   Recherchez des substituts pour les technologies qui ne seront pas portées.

    Certaines technologies, y compris DAO (Data Access Object) et le moteur de base de données Red jet, ne sont pas déplacées vers la Windows 64 bits.

-   Traitez votre version 64 bits comme une version distincte du produit.

    Même si votre produit 64 bits peut partager la même base de code que votre 32 bits, il nécessite des tests supplémentaires et peut avoir d’autres considérations relatives à la version.

## <a name="development"></a>Développement

-   Commencez à développer du code conforme maintenant.

    les développeurs peuvent commencer à écrire du code conforme en utilisant les derniers fichiers d’en-tête de Windows et les nouveaux types de données sans effets néfastes sur le développement de produits 32 bits. Pour plus d’informations, consultez [préparation à la Windows 64 bits](getting-ready-for-64-bit-windows.md).

-   Assurez-vous que votre code peut être compilé pour les Windows 32 et 64 bits.

    Le nouveau modèle de données a été conçu pour permettre la génération d’applications 32 et 64 bits à partir d’une base de code unique avec quelques modifications. les équipes de développement SQL Server et Windows développent des versions 32 et 64 bits de leurs produits à partir de la même base de code.

-   Utilisez les nouvelles fonctionnalités d’optimisation du compilateur pour obtenir de meilleures performances.

    L’optimisation du code pour les processeurs Intel Itanium est plus importante que celle de l’architecture x86. Le compilateur suppose un grand nombre des fonctions d’optimisation précédemment gérées par le microprocesseur. Vous pouvez optimiser les performances d’une application 64 bits en utilisant deux nouvelles fonctionnalités d’optimisation du compilateur : l’optimisation *guidée par profil* et l’optimisation de l’ensemble du *programme*. Les deux fonctionnalités entraînent des temps de génération plus longs et nécessitent le développement anticipé de bons scénarios de test.

    L' *optimisation guidée par profil* implique un processus de compilation en deux étapes. Au cours de la première compilation, le code est instrumenté pour capturer le comportement d’exécution. Ces informations sont utilisées lors de la deuxième compilation pour guider toutes les fonctionnalités d’optimisation.

    L’optimisation de l' *ensemble du programme* analyse le code dans tous les fichiers d’application, et pas seulement dans un seul. Cette approche augmente les performances de plusieurs façons, y compris une meilleure incorporation, ainsi qu’une analyse des effets secondaires améliorée et des conventions d’appel personnalisées.

## <a name="testing"></a>Test

-   Déterminez si vous allez tester le code 64-ou 32 bits s’exécutant dans WOW64.

    Certaines applications incluent du code 64 bits natif et du code 32 bits s’exécutant dans WOW64. Examinez cela en détail pendant le développement d’un plan de test et décidez si vos outils de test doivent être de 64 bits, 32 bits ou une combinaison. Vous devrez souvent tester les versions 64 et 32 bits de votre application sur les Windows 64 bits.

-   Testez les composants 32 bits fréquemment utilisés.

    Tout d’abord, recompilez votre code pour 64 bits et test. Ensuite, corrigez les problèmes, recompilez-les dans 32 bits, puis testez. Troisièmement, recompilez en 64 bits et testez.

-   Testez les composants COM et RPC.

    Assurez-vous que les composants COM et RPC 32 et 64 bits communiquent correctement. Vous devrez peut-être également tester les communications avec des composants 16 bits sur un réseau.

-   Testez votre version 32 bits sur le Windows 64 bits.

    les clients peuvent continuer à utiliser des applications 32 bits sur 64 bits Windows, où les problèmes de performances et de mémoire ne sont pas des considérations majeures.

-   Testez différentes configurations de mémoire.

    L’ajout de grandes quantités de mémoire sur le serveur expose parfois des problèmes précédemment inaperçus dans l’application ou le système d’exploitation.

 

 




