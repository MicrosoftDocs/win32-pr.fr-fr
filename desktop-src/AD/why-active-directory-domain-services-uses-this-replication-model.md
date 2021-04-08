---
title: Pourquoi Active Directory Domain Services utilise ce modèle de réplication
description: Cette rubrique explique les raisons du système de forme libre utilisé par Active Directory Domain Services pour un modèle de réplication.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Active Directory du modèle de réplication, avantages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538fe291a04953d373ff3cd45cbd4693d3dafab4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839257"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a>Pourquoi Active Directory Domain Services utilise ce modèle de réplication

Cette rubrique explique les raisons du système de forme libre utilisé par Active Directory Domain Services pour un modèle de réplication.

Les Active Directory Domain Services sont un système de forme libre pour les raisons suivantes :

-   Les clients ont besoin d’une solution hautement distribuée dans laquelle des parties de l’annuaire peuvent être réparties sur leurs réseaux et administrées localement.
-   Les clients de grande taille se développent souvent en millions d’objets, de centaines ou de milliers de réplicas, ou les deux.
-   De nombreux réseaux clients fournissent uniquement une connectivité intermittente à certains emplacements. par exemple, les plates-formes de forages pétroliers distantes et les navires en mer, le système doit être tolérant aux opérations partiellement connectées ou déconnectées.

Il n’existe aucun moyen de garantir la connaissance complète de l’état actuel ou futur d’un système distribué, car la connaissance des changements d’État doit être propagée et la propagation prend du temps, au cours de laquelle des modifications d’État supplémentaires peuvent se produire.

Les systèmes étroitement couplés gèrent l’incertitude en tentant de l’éliminer. Cela s’effectue par le biais de contraintes sur les mises à jour, nécessitant la disponibilité de tous les nœuds ou de la majorité des nœuds avant que les mises à jour puissent être effectuées, en utilisant des schémas de verrouillage distribués ou une simple maîtrise pour les ressources critiques, en limitant la connexion de tous les nœuds, ou une combinaison de ces techniques. Plus les nœuds informatiques sont étroitement couplés dans un système distribué, plus la limite de mise à l’échelle est faible.

Les systèmes de forme libre gèrent l’incertitude en le tolérant. Un système de forme libre permet aux nœuds d’avoir des vues différentes de l’état général du système et fournit des algorithmes pour la résolution des conflits.

Les solutions fortement couplées ont été rejetées comme inappropriées pour les Active Directory Domain Services en raison des exigences liées à l’administration locale, au fonctionnement déconnecté et à l’évolutivité vers un très grand nombre de nœuds. Le modèle faiblement couplé choisi, à compatibilité avec la cohérence multimaître avec la convergence, satisfait à toutes les exigences.

 

 




