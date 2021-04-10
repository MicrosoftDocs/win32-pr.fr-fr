---
title: Modèles de Memory-Management
description: Modèles de Memory-Management
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8114f11755829be9d5f7b17b751e075701ac0aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940347"
---
# <a name="memory-management-models"></a><span data-ttu-id="c5e12-103">Modèles de Memory-Management</span><span class="sxs-lookup"><span data-stu-id="c5e12-103">Memory-Management Models</span></span>

<span data-ttu-id="c5e12-104">En tant que développeur, vous avez plusieurs possibilités pour allouer et libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="c5e12-104">As a developer, you have several choices for how memory is allocated and freed.</span></span> <span data-ttu-id="c5e12-105">Imaginez une structure de données complexe qui se compose de nœuds connectés à des pointeurs, tels qu’une liste liée ou une arborescence.</span><span class="sxs-lookup"><span data-stu-id="c5e12-105">Consider a complex data structure that consists of nodes connected with pointers, such as a linked list or a tree.</span></span> <span data-ttu-id="c5e12-106">Vous pouvez appliquer des attributs qui sélectionnent l’un des modèles suivants :</span><span class="sxs-lookup"><span data-stu-id="c5e12-106">You can apply attributes that select one of the following models:</span></span>

-   <span data-ttu-id="c5e12-107">[Allocation et désallocation de nœud par nœud](node-by-node-allocation-and-deallocation.md).</span><span class="sxs-lookup"><span data-stu-id="c5e12-107">[Node-by-node allocation and deallocation](node-by-node-allocation-and-deallocation.md).</span></span>
-   <span data-ttu-id="c5e12-108">[Une seule mémoire tampon linéaire allouée par le stub pour l’arborescence entière](stub-allocated-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="c5e12-108">[A single linear buffer allocated by the stub for the entire tree](stub-allocated-buffers.md).</span></span>
-   [<span data-ttu-id="c5e12-109">Gestion de la mémoire stub serveur</span><span class="sxs-lookup"><span data-stu-id="c5e12-109">Server stub memory management</span></span>](server-stub-memory-management.md)
-   <span data-ttu-id="c5e12-110">[Une seule mémoire tampon linéaire allouée par l’application cliente pour l’arborescence entière](application-allocated-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="c5e12-110">[A single linear buffer allocated by the client application for the entire tree](application-allocated-buffer.md).</span></span>
-   <span data-ttu-id="c5e12-111">[Stockage persistant sur le serveur](persistent-storage-on-the-server.md).</span><span class="sxs-lookup"><span data-stu-id="c5e12-111">[Persistent storage on the server](persistent-storage-on-the-server.md).</span></span>

 

 




