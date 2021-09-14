---
description: Le fait de cliquer sur exécuter des experts dans la fenêtre experts de l’interface utilisateur du Moniteur réseau démarre les experts sélectionnés pour le fichier de capture et appelle la fonction exécuter. Une fois démarré, l’expert analyse le fichier de capture à l’aide de plusieurs fonctions de cadre d’experts.
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: Démarrer et exécuter des experts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bd41472d286727541d26bade1942eb3b6b5c593
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194547"
---
# <a name="starting-and-running-experts"></a>Démarrer et exécuter des experts

Le fait de cliquer sur **exécuter des experts** dans la fenêtre experts de l’interface utilisateur du moniteur réseau démarre les experts sélectionnés pour le fichier de capture et appelle la fonction [**exécuter**](run.md) . Une fois démarré, l’expert analyse le fichier de capture à l’aide de plusieurs fonctions de cadre d’experts.

La fonction [**ExpertIndicateStatus**](expertindicatestatus.md) fournit des informations d’état de l’expert. Lorsque vous exécutez un expert avec Moniteur réseau, la fenêtre d’affichage de l’état des experts affiche des informations d’État mises à jour régulièrement (de 0 à 100% de la progression).

![fenêtre d’affichage de l’État expert](images/exview.png)

L’expert est actif jusqu’à ce que les données se terminent par le fichier de capture. Une fois la passe terminée, une fenêtre de observateur d’événements s’affiche. Les informations contenues dans cette fenêtre dépendent du type d’expert qui a analysé les données. L’illustration suivante montre une vue de l’expert distribution de propriétés, qui résume les données de frame analysées par l’expert.

![vue expert distribution de propriété](images/exview1.png)

Un deuxième rapport (non affiché) résume les résultats de l’expert de retransmission TCP (Transmission Control Protocol).

Vous pouvez également :

-   Créez une entrée pour une page de référence d’événement qui conseille l’utilisateur de problèmes ou de conditions détectés (comme indiqué dans la fenêtre d’analyse).
-   Créez des entrées pour les corrections suggérées ou des données explicatives qui fournissent des informations supplémentaires (comme indiqué dans la fenêtre de résolution).

Une fois que l’expert a terminé sa tâche, Moniteur réseau supprime l’expert de la mémoire active. Les experts doivent utiliser les fonctions de mémoire protégée incluses dans le kit de développement logiciel (SDK) de la plateforme. ces fonctions nettoient la mémoire si les experts échouent au moment de l’exécution.

 

 



