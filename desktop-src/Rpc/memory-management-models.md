---
title: Modèles de Memory-Management
description: Modèles de Memory-Management
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8114f11755829be9d5f7b17b751e075701ac0aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194071"
---
# <a name="memory-management-models"></a>Modèles de Memory-Management

En tant que développeur, vous avez plusieurs possibilités pour allouer et libérer de la mémoire. Imaginez une structure de données complexe qui se compose de nœuds connectés à des pointeurs, tels qu’une liste liée ou une arborescence. Vous pouvez appliquer des attributs qui sélectionnent l’un des modèles suivants :

-   [Allocation et désallocation de nœud par nœud](node-by-node-allocation-and-deallocation.md).
-   [Une seule mémoire tampon linéaire allouée par le stub pour l’arborescence entière](stub-allocated-buffers.md).
-   [Gestion de la mémoire stub serveur](server-stub-memory-management.md)
-   [Une seule mémoire tampon linéaire allouée par l’application cliente pour l’arborescence entière](application-allocated-buffer.md).
-   [Stockage persistant sur le serveur](persistent-storage-on-the-server.md).

 

 




