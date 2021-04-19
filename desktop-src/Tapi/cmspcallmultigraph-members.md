---
description: Membres CMSPCallMultiGraph
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: Membres CMSPCallMultiGraph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ee556efbbdaf679e292b6b3a33b4b0a0b6616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533911"
---
# <a name="cmspcallmultigraph-members"></a><span data-ttu-id="a8678-103">Membres CMSPCallMultiGraph</span><span class="sxs-lookup"><span data-stu-id="a8678-103">CMSPCallMultiGraph Members</span></span>

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

<span data-ttu-id="a8678-104">Les blocs d’attente stockent les informations relatives à l’attente inscrite dans le pool de threads.</span><span class="sxs-lookup"><span data-stu-id="a8678-104">The wait blocks store the information about the wait registered to the thread pool.</span></span> <span data-ttu-id="a8678-105">Il comprend les handles d’attente retournés par l’appel [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) et un pointeur vers la structure de contexte.</span><span class="sxs-lookup"><span data-stu-id="a8678-105">It includes the wait handles returned by the [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) call and a pointer to the context structure.</span></span> <span data-ttu-id="a8678-106">Chaque bloc dans le tableau est destiné à un graphique dans l’un des objets de flux.</span><span class="sxs-lookup"><span data-stu-id="a8678-106">Each block in the array is for a graph in one of the stream objects.</span></span> <span data-ttu-id="a8678-107">Le décalage d’un bloc dans ce tableau est le même que celui du flux qui possède le graphique.</span><span class="sxs-lookup"><span data-stu-id="a8678-107">The offset of a block in this array is the same as the offset of the stream that owns the graph.</span></span>

 

 
