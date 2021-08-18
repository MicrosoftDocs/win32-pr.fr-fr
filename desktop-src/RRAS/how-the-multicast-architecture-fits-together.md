---
title: Combinaison de l’architecture de multidiffusion
description: Cette section décrit un exemple de configuration et la façon dont les principaux composants s’imbriquent.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94f4ca79b9fdd6b2e2fd9e75dc61d780af4380ed958a491f69231f7d541f0aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791314"
---
# <a name="how-the-multicast-architecture-fits-together"></a>Combinaison de l’architecture de multidiffusion

Cette section décrit un exemple de configuration et la façon dont les principaux composants s’imbriquent.

L’illustration suivante montre la relation entre les différents composants d’un routeur.

![relation entre les composants du routeur Windows 2000](images/mrarch1.png)

Le gestionnaire de groupe de multidiffusion fait partie du service RRAS qui s’exécute sur un serveur qui fonctionne en tant que routeur.

Trois protocoles de routage de multidiffusion (protocole 1, protocole 2, protocole 3) sont exécutés sur le routeur. Chaque protocole peut posséder une ou plusieurs interfaces (dans cette illustration, le protocole 1 possède l’interface 1, le protocole 2 possède l’interface 2 et le protocole 3 est propriétaire de l’interface 3). Chaque interface ne peut appartenir qu’à un seul protocole de routage (en plus de IGMP, ce qui est un cas spécial).

Le gestionnaire de groupe de multidiffusion s’exécute sur le routeur et coordonne la distribution des informations de groupe entre les protocoles de routage.

L’illustration suivante montre la relation entre deux routeurs dans une architecture de multidiffusion.

![relation entre deux routeurs dans une architecture de multidiffusion](images/mrarch2.png)

Dans l’illustration précédente, le routeur 2 envoie un message de multidiffusion au réseau 2 sur l’interface 3. Le routeur 1 reçoit le message de multidiffusion du réseau 2 sur l’interface 3. Sur les deux routeurs, le protocole 3 est propriétaire de l’interface respective 3.

L’illustration suivante montre le chemin d’accès d’un message provenant d’une source de multidiffusion (à un groupe multicast) pour atteindre l’hôte qui a rejoint le groupe de multidiffusion. Les routeurs de l’illustration utilisent la même configuration que les illustrations précédentes. Toutefois, les détails de l’interface et du protocole ne sont pas affichés afin de conserver la figure en simple.

![chemin d’accès du message de la source de multidiffusion à l’hôte de destination](images/mrarch3.png)

Le scénario suivant décrit les événements qui se produisent lorsqu’un hôte rejoint un groupe de multidiffusion. Reportez-vous à l’illustration précédente pour les relations entre les différentes entités.

1.  L’hôte 1 rejoint le groupe de multidiffusion G sur le réseau 3.
2.  Le routeur 3 apprend G via IGMP.
3.  Le gestionnaire de groupe de multidiffusion sur le routeur 3 notifie le protocole 3 sur le routeur 3 qu’il existe de nouveaux récepteurs pour G.
4.  Le protocole 3 sur le routeur 3 notifie ensuite le protocole 3 sur le routeur 1 à propos de G.
5.  À son tour, le protocole 3 sur le routeur 1 notifie le gestionnaire de groupe de multidiffusion sur le routeur 1 à propos de G.
6.  Le gestionnaire de groupe de multidiffusion sur le routeur 1 notifie ensuite le protocole 1 et le protocole 2 sur G.
7.  Le protocole 2 peut informer le routeur 2 de G, si le protocole est conçu à cette fin.

Le scénario suivant décrit les événements qui se produisent lorsqu’un message est envoyé à un groupe de multidiffusion. Reportez-vous à l’illustration précédente pour les relations entre les différentes entités.

1.  Une source sur le réseau 1 envoie un message au groupe G.
2.  Le message envoyé à partir de la source est d’abord dirigé vers le routeur 2, qui le transfère ensuite au routeur 1 à l’aide de l’interface 2 (puisque le routeur 2 a été informé par le protocole 2 que les récepteurs sont présents en aval).
3.  Le routeur 1 transfère le message au routeur 3 (puisque le routeur 1 a été informé par le protocole 2 que les récepteurs sont présents en aval).
4.  Le routeur 3 envoie le message au réseau 3, et il arrive donc à l’hôte 1.

Pour plus d’informations sur l’interaction du protocole de routage multidiffusion, consultez [RFC 2715](routing-protocols-request-for-comments.md), règles d’interopérabilité pour les protocoles de routage de multidiffusion.

 

 




