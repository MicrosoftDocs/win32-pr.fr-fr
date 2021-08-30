---
title: Itinéraires et le meilleur itinéraire
description: Un itinéraire est un \ 0034 ; chemin réseau \ 0034 ; à une destination associée à un certain coût. Le coût est représenté par sa préférence administrative et sa métrique propre au protocole. Les itinéraires avec des coûts inférieurs sont préférés sur tous les autres itinéraires.
ms.assetid: c5a75308-42da-4ef9-a712-9987c87eef84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78d03821ad767561441b7fc853ebac73af420ef6c239456b1d4fac59e244af8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081059"
---
# <a name="routes-and-the-best-route"></a>Itinéraires et le meilleur itinéraire

Un itinéraire est un « chemin d’accès réseau » vers une destination qui est associée à un certain coût. Le coût est représenté par sa préférence administrative et sa métrique propre au protocole. Les itinéraires avec des coûts inférieurs sont préférés sur tous les autres itinéraires.

Une entrée d’itinéraire dans la table de routage comprend les éléments suivants :

-   Handle vers la destination
-   Propriétaire de cet itinéraire
-   Voisin (homologue) qui a fourni les informations de routage
-   Indicateurs associés à l’état de l’itinéraire
-   Indicateurs associés à l’itinéraire
-   La préférence et la métrique de l’itinéraire
-   Liste des vues auxquelles l’itinéraire appartient
-   Informations privées pour le propriétaire de l’itinéraire
-   Liste des tronçons suivants utilisés pour atteindre la destination

Les valeurs suivantes, prises ensemble, identifient de façon unique un itinéraire dans la table de routage :

-   Réseau de destination
-   Propriétaire de l’itinéraire
-   Voisin ayant fourni l’itinéraire

## <a name="metrics-and-preference"></a>Métriques et préférences

Chaque itinéraire a une préférence administrative (spécifiée par la stratégie de routage) et une mesure dépendante du client. Le gestionnaire de tables de routage utilise ces informations pour déterminer quel itinéraire est le meilleur itinéraire vers une destination. Les itinéraires avec une préférence inférieure sont de meilleurs itinéraires (l’un étant le plus bas, et par conséquent le meilleur). Si deux itinéraires ont la même préférence, l’itinéraire avec la métrique inférieure est le meilleur itinéraire.

Normalement, la préférence d’un itinéraire est déterminée par la préférence du client qui a ajouté l’itinéraire. Toutefois, pour tous les itinéraires ajoutés à l’aide de l’outil de gestion Netsh.exe, vous pouvez spécifier une valeur de préférence pour chaque itinéraire.

La préférence est normalement utilisée pour indiquer la priorité entre les clients. Par exemple, un administrateur peut attribuer à OSPF une préférence inférieure à celle de RIP. Dans ce cas, les itinéraires OSPF sont préférables aux itinéraires RIP.

 

 




