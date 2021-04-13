---
title: Fonction named_type_from_local
description: Les stubs appellent le \_ type nommé \_ à partir de la \_ fonction locale.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94606a197f3763770db8e0d455a9d0b09f5dab0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309602"
---
# <a name="the-named_type_from_local-function"></a><span data-ttu-id="0754d-104">Type nommé \_ \_ à partir de la \_ fonction locale</span><span class="sxs-lookup"><span data-stu-id="0754d-104">The named\_type\_from\_local Function</span></span>

<span data-ttu-id="0754d-105">Les stubs appellent le \_ type nommé \_ à partir de la \_ fonction locale.</span><span class="sxs-lookup"><span data-stu-id="0754d-105">The stubs call the named\_type\_from\_local function.</span></span> <span data-ttu-id="0754d-106">Il convertit le type que l’application utilise dans le type transmis par les stubs sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="0754d-106">It converts the type that the application uses into the type the stubs transmit across the network.</span></span> <span data-ttu-id="0754d-107">La fonction est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="0754d-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

<span data-ttu-id="0754d-108">Le premier paramètre est un pointeur vers les données d’application.</span><span class="sxs-lookup"><span data-stu-id="0754d-108">The first parameter is a pointer to the application data.</span></span> <span data-ttu-id="0754d-109">Le deuxième paramètre est un pointeur vers un pointeur.</span><span class="sxs-lookup"><span data-stu-id="0754d-109">The second parameter is a pointer to a pointer.</span></span> <span data-ttu-id="0754d-110">La fonction pointe vers les données transmises.</span><span class="sxs-lookup"><span data-stu-id="0754d-110">The function points it to the transmitted data.</span></span> <span data-ttu-id="0754d-111">La fonction doit allouer de la mémoire pour le type transmis.</span><span class="sxs-lookup"><span data-stu-id="0754d-111">The function must allocate memory for the transmitted type.</span></span>

 

 




