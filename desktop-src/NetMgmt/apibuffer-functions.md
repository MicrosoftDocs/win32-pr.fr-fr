---
title: ApiBuffer, fonctions
description: Les fonctions de ApiBuffer de gestion de réseau sont utilisées pour gérer l’allocation de mémoire utilisée par une application avec des fonctions de gestion de réseau.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b316c6b2ee2d4095c15d5e859dd0069978c7ff91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509452"
---
# <a name="apibuffer-functions"></a><span data-ttu-id="b12a5-103">ApiBuffer, fonctions</span><span class="sxs-lookup"><span data-stu-id="b12a5-103">ApiBuffer Functions</span></span>

<span data-ttu-id="b12a5-104">Les fonctions de ApiBuffer de gestion de réseau sont utilisées pour gérer l’allocation de mémoire utilisée par une application avec des fonctions de gestion de réseau.</span><span class="sxs-lookup"><span data-stu-id="b12a5-104">The network management ApiBuffer functions are used to manage memory allocation used by an application with network management functions.</span></span> <span data-ttu-id="b12a5-105">Toutefois, en général, pour toute autre mémoire utilisée par une application, vous devez utiliser les [fonctions de gestion](/windows/desktop/Memory/memory-management-functions) de la mémoire au lieu de ces fonctions ApiBuffer.</span><span class="sxs-lookup"><span data-stu-id="b12a5-105">However, in general, for other memory used by an application you should use the [memory management functions](/windows/desktop/Memory/memory-management-functions) instead of these ApiBuffer functions.</span></span>

<span data-ttu-id="b12a5-106">Les fonctions ApiBuffer sont répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b12a5-106">The ApiBuffer functions are listed following.</span></span>



| <span data-ttu-id="b12a5-107">Fonction</span><span class="sxs-lookup"><span data-stu-id="b12a5-107">Function</span></span>                                                 | <span data-ttu-id="b12a5-108">Description</span><span class="sxs-lookup"><span data-stu-id="b12a5-108">Description</span></span>                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b12a5-109">**NetApiBufferAllocate**</span><span class="sxs-lookup"><span data-stu-id="b12a5-109">**NetApiBufferAllocate**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | <span data-ttu-id="b12a5-110">Alloue de la mémoire à partir du tas.</span><span class="sxs-lookup"><span data-stu-id="b12a5-110">Allocates memory from the heap.</span></span> <span data-ttu-id="b12a5-111">Appelez cette fonction lorsque vous avez besoin d’une compatibilité avec la fonction **NetApiBufferFree** .</span><span class="sxs-lookup"><span data-stu-id="b12a5-111">Call this function when you require compatibility with the **NetApiBufferFree** function.</span></span> |
| [<span data-ttu-id="b12a5-112">**NetApiBufferFree**</span><span class="sxs-lookup"><span data-stu-id="b12a5-112">**NetApiBufferFree**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | <span data-ttu-id="b12a5-113">Libère de la mémoire allouée par la fonction **NetApiBufferAllocate** et d’autres fonctions de gestion de réseau.</span><span class="sxs-lookup"><span data-stu-id="b12a5-113">Frees memory allocated by the **NetApiBufferAllocate** function and other network management functions.</span></span>                   |
| [<span data-ttu-id="b12a5-114">**NetApiBufferReallocate**</span><span class="sxs-lookup"><span data-stu-id="b12a5-114">**NetApiBufferReallocate**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | <span data-ttu-id="b12a5-115">Modifie la taille d’une mémoire tampon allouée par un appel à la fonction **NetApiBufferAllocate** .</span><span class="sxs-lookup"><span data-stu-id="b12a5-115">Changes the size of a buffer allocated by a call to the **NetApiBufferAllocate** function.</span></span>                                |
| [<span data-ttu-id="b12a5-116">**NetApiBufferSize**</span><span class="sxs-lookup"><span data-stu-id="b12a5-116">**NetApiBufferSize**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | <span data-ttu-id="b12a5-117">Retourne la taille, en octets, d’une mémoire tampon allouée par un appel à la fonction **NetApiBufferAllocate** .</span><span class="sxs-lookup"><span data-stu-id="b12a5-117">Returns the size, in bytes, of a buffer allocated by a call to the **NetApiBufferAllocate** function.</span></span>                     |



 

<span data-ttu-id="b12a5-118">Pour les fonctions accessibles à distance qui retournent des informations à l’appelant, la bibliothèque Runtime RPC alloue la mémoire tampon contenant les informations de retour.</span><span class="sxs-lookup"><span data-stu-id="b12a5-118">For remotable functions that return information to the caller, the RPC run-time library allocates the buffer containing the return information.</span></span> <span data-ttu-id="b12a5-119">Lorsque l’appelant a fini de traiter les informations, il doit appeler la fonction [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) pour libérer la mémoire tampon allouée.</span><span class="sxs-lookup"><span data-stu-id="b12a5-119">When the caller has finished processing the information, it must call the [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) function to free the allocated buffer.</span></span>

 

 