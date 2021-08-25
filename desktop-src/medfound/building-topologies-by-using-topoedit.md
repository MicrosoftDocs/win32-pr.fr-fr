---
description: Création de topologies à l’aide de TopoEdit
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: Création de topologies à l’aide de TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e678e0c25cbfe56c2633091820468a6c0313663847870a4de5c912a5edae95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959433"
---
# <a name="building-topologies-by-using-topoedit"></a>Création de topologies à l’aide de TopoEdit

Une topologie doit avoir les trois nœuds suivants :

-   Nœud source : flux d’un fichier multimédia, qui sont utilisés comme source pour la topologie.
-   Nœud de transformation : une transformation de Media Foundation (MFT). Ces nœuds sont généralement des encodeurs, des décodeurs et des effets pour la topologie.
-   Nœud de sortie : récepteur de flux qui transmet les données multimédia, les images vidéo ou les flux audio à la session multimédia pour la lecture.

Pour plus d’informations sur la structure de la topologie, consultez [à propos des topologies](about-topologies.md).

Pour créer une topologie, vous devez ajouter les nœuds, connecter les nœuds et résoudre la topologie de manière à ce qu’elle puisse être lue.

Les nœuds de topologie sont affichés sous forme de zones, avec un texte affichant le nom du nœud. Les zones vertes représentent les nœuds ajoutés par l’utilisateur. Quand une topologie est résolue, TopoEdit peut ajouter automatiquement des nœuds de transformation à la topologie. Celles-ci apparaissent sous forme de zones bleues dans le **volet Topology**.

Les entrées et sorties de topologie sont représentées par des carrés noirs le long du bord du nœud. L' *entrée de nœud* s’affiche sur le côté gauche du nœud, et la *sortie du nœud* se trouve à droite du nœud.

Les nœuds de topologie sont connectés via une *connexion de nœud* qui s’affiche sous la forme d’une ligne noire connectant l’entrée de nœud d’un nœud à la sortie de nœud d’un autre nœud.

L’illustration suivante montre une topologie connectée pour une source audio.

![Illustration montrant les connexions du nœud source, à deux nœuds de transformation, puis au nœud de sortie](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

Cette section contient les rubriques suivantes :



| Rubrique                                                                                          | Description                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Ajout de nœuds sources avec TopoEdit](adding-source-nodes-with-topoedit.md)                     | Décrit le processus d’ajout de nœuds sources à une topologie.    |
| [Ajout de nœuds de transformation avec TopoEdit](adding-transform-nodes-with-topoedit.md)               | Décrit le processus d’ajout de nœuds de transformation à une topologie. |
| [Ajout de nœuds de sortie avec TopoEdit](adding-output-nodes-with-topoedit.md)                     | Décrit le processus d’ajout de nœuds de sortie à une topologie.    |
| [Connexion et déconnexion des nœuds de topologie](connecting-and-disconnecting-topology-nodes.md) | Décrit le processus de connexion de deux nœuds.                 |
| [Résolution d’une topologie avec TopoEdit](resolving-a-topology-with-topoedit.md)                   | Décrit le processus de résolution de la topologie.                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



