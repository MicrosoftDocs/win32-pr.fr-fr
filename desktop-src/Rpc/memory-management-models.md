---
title: Modèles de Memory-Management
description: Modèles de Memory-Management
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a985158f54bf09d149e04c7eebc5853417e39191ca0bb854cb7d1ba5de1e5d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019979"
---
# <a name="memory-management-models"></a>Modèles de Memory-Management

En tant que développeur, vous avez plusieurs possibilités pour allouer et libérer de la mémoire. Imaginez une structure de données complexe qui se compose de nœuds connectés à des pointeurs, tels qu’une liste liée ou une arborescence. Vous pouvez appliquer des attributs qui sélectionnent l’un des modèles suivants :

-   [Allocation et désallocation de nœud par nœud](node-by-node-allocation-and-deallocation.md).
-   [Une seule mémoire tampon linéaire allouée par le stub pour l’arborescence entière](stub-allocated-buffers.md).
-   [Gestion de la mémoire stub serveur](server-stub-memory-management.md)
-   [Une seule mémoire tampon linéaire allouée par l’application cliente pour l’arborescence entière](application-allocated-buffer.md).
-   [Stockage persistant sur le serveur](persistent-storage-on-the-server.md).

 

 




