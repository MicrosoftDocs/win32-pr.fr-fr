---
title: Protocole de routage
description: Un protocole de routage est un type de client qui s’inscrit auprès du gestionnaire de tables de routage. Les routeurs utilisent des protocoles de routage pour échanger des informations relatives aux itinéraires vers une destination.
ms.assetid: 957ec896-94e3-4bdb-801a-12b861460fff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e64d12912494d0d6c20f484eba588b47670a808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029115"
---
# <a name="routing-protocol"></a>Protocole de routage

Un protocole de routage est un type de client qui s’inscrit auprès du gestionnaire de tables de routage. Les routeurs utilisent des protocoles de routage pour échanger des informations relatives aux itinéraires vers une destination.

Les protocoles de routage sont monodiffusion ou multidiffusion. Les protocoles de routage publient les itinéraires vers une destination.

Un itinéraire de monodiffusion vers une destination est utilisé par un protocole de routage monodiffusion pour transmettre les données de monodiffusion à cette destination. Voici des exemples de protocoles de routage monodiffusion : RIP (Routing Information Protocol), OSPF (Open Shortest Path First) et Border Gateway Protocol (BGP).

Un itinéraire de multidiffusion vers une destination est utilisé par certains protocoles de routage de multidiffusion pour créer les informations utilisées pour transférer des données de multidiffusion à partir d’hôtes sur le réseau de destination de l’itinéraire (appelé transfert de chemin inverse). Voici des exemples de protocoles de routage de multidiffusion : MOSPF (multicast Open Shortest Path First), DVMRP (distance Vector Multicast Routing Protocol) et PIM (Protocol Independent multicast).

Le gestionnaire de tables de routage prend en charge plusieurs instances du même protocole (telles que l’implémentation de OSPF par Microsoft et un protocole OSPF tiers) exécuté sur le routeur. Cela permet aux routeurs d’utiliser les différentes fonctionnalités de chaque version. Ces protocoles ont des identificateurs de protocole différents.

Les identificateurs de protocole sont constitués d’un identificateur de fournisseur et d’un identificateur spécifique au protocole. L’identificateur propre au protocole est le même pour les différentes implémentations du protocole, telles que l’implémentation de OSPF par Microsoft et une implémentation tierce de OSPF. Un identificateur unique est associé à un protocole de routage uniquement lorsque les identificateurs spécifiques au fournisseur et au protocole sont combinés.

Un protocole avec le même identificateur de protocole (autrement dit, un identificateur de fournisseur et un identificateur propre au protocole) peut s’inscrire plusieurs fois auprès du gestionnaire de tables de routage. Chaque fois, le protocole s’inscrit à l’aide d’un identificateur d’instance de protocole différent. Par exemple, une implémentation de OSPF à partir d’un fournisseur particulier peut s’inscrire en tant que Vendor-OSPF-1 et Vendor-OSPF-2. Cela permet à une implémentation de protocole spécifique de partitionner les informations qu’elle conserve dans la table de routage.

 

 




