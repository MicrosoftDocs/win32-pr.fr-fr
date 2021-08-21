---
description: Utilisation du CRM COM+ dans un environnement de cluster
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: Utilisation du CRM COM+ dans un environnement de cluster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31a2d0800f98c9453e7d4454cdd59185dffb837649e391ebc415c965bee6ff80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499529"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a>Utilisation du CRM COM+ dans un environnement de cluster

Lorsque vous développez des CRM CRM pour travailler dans des environnements de cluster, le principal facteur à prendre en compte est de savoir si un CRM spécifique détermine quel nœud du cluster sur lequel il est en cours d’utilisation. Par exemple, si la ressource gérée par le CRM est le système de fichiers de l’ordinateur ou le registre, toute modification est spécifique au nœud sur lequel l’application CRM Server est exécutée à ce moment-là. Dans ce cas, le basculement de l’application CRM Server vers un autre nœud n’est pas souhaitable. Dans un cas différent, où le CRM gère des ressources communes au cluster, le basculement de l’application CRM Server vers un autre nœud est utile.

L’emplacement du répertoire par défaut pour les fichiers journaux CRM est le même que celui du fichier journal DTC. Sur les clusters, le fichier journal DTC est placé sur un disque partagé qui est basculé entre les nœuds du cluster. Cela signifie que le comportement par défaut pour les applications serveur CRM est le basculement entre les nœuds du cluster. Par conséquent, si un CRM spécifique requiert un autre comportement qui consiste à ne pas basculer entre les nœuds, l’emplacement du fichier journal CRM pour cette application CRM Server particulière doit être modifié.

En outre, si le basculement est requis pour l’application CRM, il doit être configuré en tant qu’application générique dans un groupe de clusters. Sa dépendance doit être DTC.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de Gestionnaire des ressources de compensation COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



