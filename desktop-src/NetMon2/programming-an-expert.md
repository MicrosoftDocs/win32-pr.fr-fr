---
description: Le kit de développement logiciel (SDK) Moniteur réseau comprend les fonctions et les exemples de code dont vous avez besoin pour créer des experts. Toutefois, vous pouvez également utiliser des outils existants, y compris un éditeur de boîtes de dialogue.
ms.assetid: 6a3834b7-753f-42cc-986f-3d7e8bf79fd9
title: Programmation d’un expert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38de0a60c8224ce0912039ea5fbb06e2cdc958e317eccfb83d524ce632b0d539
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979179"
---
# <a name="programming-an-expert"></a>Programmation d’un expert

Le kit de développement logiciel (SDK) Moniteur réseau comprend les fonctions et les exemples de code dont vous avez besoin pour créer des experts. Toutefois, vous pouvez également utiliser des outils existants, y compris un éditeur de boîtes de dialogue.

## <a name="minimum-requirements-to-run-an-expert"></a>Configuration minimale requise pour exécuter un expert

Le tableau suivant répertorie les points d’entrée de DLL et les fonctions d’experts que vous devez utiliser pour créer un expert.



| Nom                                                 | Type               | Requis ?                                       |
|------------------------------------------------------|--------------------|-------------------------------------------------|
| [**DllMain**](dllmain-expert.md)                    | Fonction d’entrée de DLL | Oui                                             |
| [**Inscrire un expert**](register-expert.md)           | Fonction d’entrée de DLL | Oui                                             |
| [**Exécuter**](run.md)                                   | Fonction d’entrée de DLL | Oui                                             |
| [**Configurer**](configure.md)                       | Fonction d’entrée de DLL | Uniquement si l’expert fournit la configuration utilisateur. |
| [**ExpertIndicateStatus**](expertindicatestatus.md) | Fonction expert    | Oui                                             |
| [**ExpertSubmitEvent**](expertsubmitevent.md)       | Fonction expert    | Oui                                             |



 

Consultez les rubriques de référence de l’expert et de l’analyseur dans le kit de développement logiciel (SDK) Moniteur réseau pour mettre à jour votre code source, puis utilisez l’exemple de code et les procédures fournis dans les rubriques suivantes :

-   [Création d’un expert](building-an-expert.md)
-   [Installation d’un expert](installing-an-expert-to-network-monitor-2-1.md)
-   [Débogage d’un expert](debugging-an-expert.md)

Les dll d’experts requièrent le C, et non la Convention d’appel C++, car les fonctions sont appelées par le biais de pointeurs de fonction à l’aide d’une superposition. Grâce à un ensemble de fonctions d’experts spécialisées, l’expert a accès aux frames de la capture. L’expert peut utiliser la plupart des Moniteur réseau API pour manipuler les données renvoyées. Lorsqu’un expert trouve des informations à envoyer à l’utilisateur, il reporte les informations dans une structure de données d’événement et les soumet à Moniteur réseau, qui affiche ensuite les informations dans une fenêtre de sortie d’expert. L’expert doit régulièrement mettre à jour Moniteur réseau avec des informations d’état d’achèvement de pourcentage, qui sont fournies par la fonction [**ExpertIndicateStatus**](expertindicatestatus.md) .

Les fonctions exportées par l’expert sont appelées comme suit :

-   Lorsque Moniteur réseau crée la liste d’experts à présenter à l’utilisateur, Moniteur réseau appelle la fonction d' [**expert d’inscription**](register-expert.md) .
-   Après l’appel à **Register**, si l’expert est configurable, moniteur réseau appelle la fonction [**configure**](configure.md) .
-   Lorsque l’utilisateur Moniteur réseau clique sur **exécuter expert**, moniteur réseau appelle la fonction [**Run**](run.md) .

Quand les experts analysent les trames demandées et trouvent un problème, ils utilisent [**ExpertSubmitEvent**](expertsubmitevent.md) pour envoyer un événement qui contient des informations sur le problème. Moniteur réseau distribue l’événement au observateur d’événements standard (partagé) ou (si l’expert s’inscrit pour lui) sur un observateur d’événements privé.

 

 



