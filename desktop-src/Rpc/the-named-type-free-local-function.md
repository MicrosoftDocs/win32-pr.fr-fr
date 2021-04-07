---
title: Fonction named_type_free_local
description: Les stubs appellent la \_ \_ fonction locale Free de type pour libérer la mémoire allouée par un appel au \_ type nommé à la \_ \_ routine locale.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f2796f33e9dc60364b6afda244d8dae47eef0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672258"
---
# <a name="the-named_type_free_local-function"></a><span data-ttu-id="26c93-104">\_ \_ Fonction locale Free de type nommé \_</span><span class="sxs-lookup"><span data-stu-id="26c93-104">The named\_type\_free\_local Function</span></span>

<span data-ttu-id="26c93-105">Les stubs appellent la fonction **\_ \_ locale Free de type** pour libérer la mémoire allouée par un appel au [type nommé à la routine \_ \_ \_ locale](the-named-type-to-local-function.md) .</span><span class="sxs-lookup"><span data-stu-id="26c93-105">The stubs call the **type\_free\_local** function to free the memory allocated by a call to the [named\_type\_to\_local](the-named-type-to-local-function.md) routine.</span></span> <span data-ttu-id="26c93-106">Elle ne libère pas la mémoire allouée par le stub.</span><span class="sxs-lookup"><span data-stu-id="26c93-106">It does not free the memory allocated by the stub.</span></span> <span data-ttu-id="26c93-107">Le prototype de fonction est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="26c93-107">The function prototype is defined as:</span></span>

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

<span data-ttu-id="26c93-108">Le paramètre est un pointeur vers la mémoire allouée par le **\_ type nommé \_ à \_ local**.</span><span class="sxs-lookup"><span data-stu-id="26c93-108">The parameter is a pointer to the memory allocated by **named\_type\_to\_local**.</span></span>

 

 




