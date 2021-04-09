---
title: Pointeurs et allocation de mémoire
description: La possibilité de modifier la mémoire par le biais de pointeurs requiert souvent que le serveur et le client allouent suffisamment de mémoire pour les éléments du tableau.
ms.assetid: 8a49582a-9ae4-4f26-a172-bc8fe2aab65a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdd4c51207de093dfe2d32ec0c275aa7a05a317
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102121"
---
# <a name="pointers-and-memory-allocation"></a><span data-ttu-id="dd573-103">Pointeurs et allocation de mémoire</span><span class="sxs-lookup"><span data-stu-id="dd573-103">Pointers and Memory Allocation</span></span>

<span data-ttu-id="dd573-104">La possibilité de modifier la mémoire par le biais de pointeurs requiert souvent que le serveur et le client allouent suffisamment de mémoire pour les éléments du tableau.</span><span class="sxs-lookup"><span data-stu-id="dd573-104">The ability to change memory through pointers often requires that the server and the client allocate enough memory for the elements in the array.</span></span>

<span data-ttu-id="dd573-105">Quand un stub doit allouer ou libérer de la mémoire, il appelle des fonctions de la bibliothèque Runtime qui, à leur tour, appellent les fonctions [**MIDL \_ User \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) et [**MIDL \_ User \_ Free**](/windows/desktop/Midl/midl-user-free-1).</span><span class="sxs-lookup"><span data-stu-id="dd573-105">When a stub must allocate or free memory, it calls run-time library functions that in turn call the functions [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) and [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1).</span></span> <span data-ttu-id="dd573-106">Ces fonctions ne sont pas incluses dans la bibliothèque Runtime.</span><span class="sxs-lookup"><span data-stu-id="dd573-106">These functions are not included as part of the run-time library.</span></span> <span data-ttu-id="dd573-107">Vous devez écrire vos propres versions de ces fonctions et les lier à votre application.</span><span class="sxs-lookup"><span data-stu-id="dd573-107">You need to write your own versions of these functions and link them with your application.</span></span> <span data-ttu-id="dd573-108">De cette façon, vous pouvez décider comment gérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="dd573-108">In this way, you can decide how to manage memory.</span></span> <span data-ttu-id="dd573-109">Lors de la compilation de votre fichier IDL en mode compatibilité OSF (**/OSF**), il n’est pas nécessaire d’implémenter ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="dd573-109">When compiling your IDL file in OSF-compatibility (**/osf**) mode, you do not need to implement these functions.</span></span> <span data-ttu-id="dd573-110">Vous devez écrire ces fonctions dans les prototypes suivants :</span><span class="sxs-lookup"><span data-stu-id="dd573-110">You must write these functions to the following prototypes:</span></span>

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
```

<span data-ttu-id="dd573-111">Par exemple, les versions de ces fonctions pour une application peuvent simplement appeler des fonctions de bibliothèque standard :</span><span class="sxs-lookup"><span data-stu-id="dd573-111">For example, the versions of these functions for an application can simply call standard library functions:</span></span>


```C++
void __RPC_FAR * __RPC_API midl_user_allocate(size_t len)
{
    return(malloc(len));
}

void __RPC_API midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 