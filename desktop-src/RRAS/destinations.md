---
title: Destinations
description: Une destination dans la table de routage est une entrée réseau représentée par une adresse réseau et un masque de réseau.
ms.assetid: 115d86e3-f933-4601-af10-abaab287b509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88195bb0bffab46495693f79a5e4329ec0e83c801c8ee4cf50d8d8bbe39b9ac0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961129"
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

 

 




