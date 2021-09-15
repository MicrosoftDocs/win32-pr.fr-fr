---
description: Création de topologies
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Création de topologies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ec738c82ea2b85bcae7d4c05627b81ad939db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524284"
---
# <a name="creating-topologies"></a>Création de topologies

Cette section décrit quelques-unes des procédures générales pour la création d’une topologie.

Les étapes générales de la création d’une topologie sont les suivantes :

1.  Créez un nouvel objet topologique en appelant [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology). Cette fonction retourne un pointeur vers l’interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topologie.

2.  Au départ, la topologie ne contient aucun nœud. Pour créer des nœuds pour la topologie, appelez [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode). Cette fonction retourne un pointeur vers l’interface [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) du nœud. Vous devez spécifier le type de nœud lorsque vous créez le nœud :

    -   Nœud source.

    -   Nœud transformer.

    -   Nœud de sortie.

    -   Nœud tee.

3.  Initialisez chaque nœud. Le processus d’initialisation dépend du type de nœud, comme décrit dans les rubriques qui suivent.

4.  Ajoutez chaque nœud à la topologie en appelant [**IMFTopology :: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).

5.  Connecter les nœuds. Pour connecter un nœud, appelez [**IMFTopologyNode :: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) sur le nœud amont, puis transmettez un pointeur vers le nœud en aval.

Les rubriques suivantes fournissent les étapes spécifiques pour chaque type de nœud.



| Rubrique                                                    | Description                     |
|----------------------------------------------------------|---------------------------------|
| [Création de nœuds sources](creating-source-nodes.md)       | Comment créer un nœud source.    |
| [Création de nœuds de transformation](creating-transform-nodes.md) | Comment créer un nœud de transformation. |
| [Création de nœuds de sortie](creating-output-nodes.md)       | Comment créer un nœud de sortie.   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Topologies](topologies.md)
</dt> </dl>

 

 



