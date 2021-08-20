---
description: Connexion et déconnexion des nœuds de topologie
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: Connexion et déconnexion des nœuds de topologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6113f4648d0aafbe41dc13090dc83807f746f0acc945f76eca0acf1b4898913f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064625"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a>Connexion et déconnexion des nœuds de topologie

Pour qu’une topologie soit fonctionnelle, le nœud source et le nœud de sortie doivent être connectés. Pour connecter deux nœuds de topologie, faites glisser la sortie de nœud d’un nœud vers l’entrée de nœud de l’autre nœud. TopoEdit affiche la connexion de nœud sous la forme d’une ligne noire. Cela équivaut à connecter des nœuds de topologie en appelant la méthode [**IMFTopologyNode :: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) .

La topologie peut être résolue uniquement si la connexion au nœud est valide ; autrement dit, si les types de média des deux nœuds sont compatibles. Pour plus d’informations sur la résolution des topologies, consultez [résolution d’une topologie à l’aide de TopoEdit](resolving-a-topology-with-topoedit.md).

Si vous tentez d’établir une connexion à partir d’un nœud qui est déjà connecté, la nouvelle connexion de nœud remplace l’ancienne connexion de nœud.

Pour supprimer une connexion, sélectionnez la connexion de nœud et appuyez sur la touche SUPPR ou sélectionnez **supprimer** dans le menu **Topology (topologie** ).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de topologies à l’aide de TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



