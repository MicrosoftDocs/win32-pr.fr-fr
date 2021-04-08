---
title: Destinations
description: Une destination dans la table de routage est une entrée réseau représentée par une adresse réseau et un masque de réseau.
ms.assetid: 115d86e3-f933-4601-af10-abaab287b509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c0c758720824284147c2f35be004622157edb3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840162"
---
# <a name="destinations"></a>Destinations

Une destination dans la table de routage est une entrée réseau représentée par une adresse réseau et un masque de réseau.

Une entrée de destination dans la table de routage comprend les éléments suivants :

-   Adresse, exprimée sous la forme d’une adresse réseau et d’un masque de réseau.
-   Liste des itinéraires vers la destination.
-   Liste d’emplacements de pointeurs opaques.
-   Vues dans lesquelles cette destination est valide. La destination contient une structure pour chaque vue qui contient les informations suivantes :
    -   Identificateur de la vue.
    -   Pointeur vers le meilleur itinéraire vers la destination dans cette vue.
    -   Propriétaire du meilleur itinéraire dans cette vue.
    -   Indicateurs associés au meilleur itinéraire dans cette vue.
    -   Handle vers tous les itinéraires qui sont dans un état de blocage dans cette vue.

 

 




