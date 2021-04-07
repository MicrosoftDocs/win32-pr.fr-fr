---
title: Détection et prévention de la latence de réplication
description: La latence de réplication est un fait de la vie dans un système distribué faiblement couplé.
ms.assetid: ea65759b-2bfa-4859-8d2a-5949bbb9adef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271b4d84689068824a6e46095a5ed93462f49e2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671346"
---
# <a name="detecting-and-avoiding-replication-latency"></a>Détection et prévention de la latence de réplication

La latence de réplication est un fait de la vie dans un système distribué faiblement couplé. Les applications doivent prendre en charge ce. La meilleure façon de prendre en charge la latence de réplication consiste à concevoir des applications pour réduire les effets. L’application idéale pour les annuaires :

-   N’est pas sensible au décalage de version.
-   Ne dépend pas des relations entre plusieurs objets.
-   N’a aucune exigence de cohérence intra-ou inter-objets.

Les applications et services qui correspondent à ce profil n’ont pas besoin de la latence de réplication. D’autres applications doivent être conçues avec une latence de réplication à l’esprit. La clé de la réussite de la conception d’une telle application est la reconnaissance du processus de réplication. Étapes effectuées au moment de la conception pour réduire les dépendances entre les objets et réduire le nombre de retards de mise à jour partielle au moment de l’exécution. Les approches de la latence de la réplication sont divisées en deux classes : des stratégies d’évitement qui réduisent l’impact des stratégies de latence et de détection qui permettent à une application de détecter les États induits par la latence.

 

 




