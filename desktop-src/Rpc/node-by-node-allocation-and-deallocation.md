---
title: Allocation et désallocation de nœud par nœud
description: L’allocation nœud par nœud et la désallocation des structures de données par les stubs sont la méthode par défaut de gestion de la mémoire pour tous les paramètres sur le client et le serveur.
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cc6b3ff61d4db3ba716664a2ff854e94cb28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463406"
---
# <a name="node-by-node-allocation-and-deallocation"></a><span data-ttu-id="4e6ae-103">Allocation et désallocation de nœud par nœud</span><span class="sxs-lookup"><span data-stu-id="4e6ae-103">Node-by-Node Allocation and Deallocation</span></span>

<span data-ttu-id="4e6ae-104">L’allocation nœud par nœud et la désallocation des structures de données par les stubs sont la méthode par défaut de gestion de la mémoire pour tous les paramètres sur le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="4e6ae-104">Node-by-node allocation and deallocation of data structures by the stubs is the default method of memory management for all parameters on both the client and the server.</span></span> <span data-ttu-id="4e6ae-105">Côté client, le stub alloue chaque nœud avec un appel distinct à l' [ \_ \_ allocation d’utilisateur MIDL](/windows/desktop/Midl/midl-user-allocate-1).</span><span class="sxs-lookup"><span data-stu-id="4e6ae-105">On the client side, the stub allocates each node with a separate call to [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1).</span></span> <span data-ttu-id="4e6ae-106">Côté serveur, au lieu d’appeler l' **\_ \_ allocation d’utilisateur MIDL**, la mémoire privée est utilisée chaque fois que cela est possible.</span><span class="sxs-lookup"><span data-stu-id="4e6ae-106">On the server side, rather than calling **midl\_user\_allocate**, private memory is used whenever possible.</span></span> <span data-ttu-id="4e6ae-107">Si **l' \_ \_ allocation d’utilisateur MIDL** est appelée, les stubs de serveur appellent **MIDL \_ User \_ Free** pour libérer les données.</span><span class="sxs-lookup"><span data-stu-id="4e6ae-107">If **midl\_user\_allocate** is called, the server stubs will call **midl\_user\_free** to free the data.</span></span> <span data-ttu-id="4e6ae-108">Dans la plupart des cas, l’utilisation de l’allocation et de la désallocation nœud par nœud au lieu d’utiliser **\[ allocate (tous les \_ nœuds) \]** entraîne une augmentation des performances des stubs côté serveur.</span><span class="sxs-lookup"><span data-stu-id="4e6ae-108">In most cases, using node-by-node allocation and deallocation instead of using **\[allocate (all\_nodes)\]** will result in increased performance of the server side stubs.</span></span>

 

 