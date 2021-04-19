---
title: Capacité. COTISATIONS
description: Dans l’exemple de composant fournisseur, un exemple de code qui montre l’allocation et la libération de mémoire se trouve dans Memory. cpp. Les routines prises en charge sont répertoriées dans le tableau suivant.
ms.assetid: dc5b3559-02fc-45e8-bbd0-482e4e3a7f8a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9add77dcdbbfc0ddab547cd537b352c9a68bdaf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512634"
---
# <a name="memorycpp"></a><span data-ttu-id="5ca23-104">Capacité. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="5ca23-104">MEMORY.CPP</span></span>

<span data-ttu-id="5ca23-105">Dans l’exemple de composant fournisseur, un exemple de code qui montre l’allocation et la libération de mémoire se trouve dans Memory. cpp.</span><span class="sxs-lookup"><span data-stu-id="5ca23-105">In the example provider component, a code example showing memory allocation and freeing is in memory.cpp.</span></span> <span data-ttu-id="5ca23-106">Les routines prises en charge sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5ca23-106">Supported routines are listed in the following table.</span></span>



| <span data-ttu-id="5ca23-107">Élément</span><span class="sxs-lookup"><span data-stu-id="5ca23-107">Item</span></span>                | <span data-ttu-id="5ca23-108">Description</span><span class="sxs-lookup"><span data-stu-id="5ca23-108">Description</span></span>                                                           |
|---------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="5ca23-109">**AllocProvMem**</span><span class="sxs-lookup"><span data-stu-id="5ca23-109">**AllocProvMem**</span></span>    | <span data-ttu-id="5ca23-110">Allouer la mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5ca23-110">Allocate specified memory.</span></span>                                            |
| <span data-ttu-id="5ca23-111">**FreeProvMem**</span><span class="sxs-lookup"><span data-stu-id="5ca23-111">**FreeProvMem**</span></span>     | <span data-ttu-id="5ca23-112">Mémoire disponible indiquée.</span><span class="sxs-lookup"><span data-stu-id="5ca23-112">Free memory indicated.</span></span>                                                |
| <span data-ttu-id="5ca23-113">**ReallocProvMem**</span><span class="sxs-lookup"><span data-stu-id="5ca23-113">**ReallocProvMem**</span></span>  | <span data-ttu-id="5ca23-114">Allouez de la mémoire contiguë.</span><span class="sxs-lookup"><span data-stu-id="5ca23-114">Allocate contiguous memory.</span></span>                                           |
| <span data-ttu-id="5ca23-115">**AllocProvStr**</span><span class="sxs-lookup"><span data-stu-id="5ca23-115">**AllocProvStr**</span></span>    | <span data-ttu-id="5ca23-116">Allouez une chaîne LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="5ca23-116">Allocate an LPWSTR string.</span></span>                                            |
| <span data-ttu-id="5ca23-117">**FreeProvStr**</span><span class="sxs-lookup"><span data-stu-id="5ca23-117">**FreeProvStr**</span></span>     | <span data-ttu-id="5ca23-118">Chaîne libre si elle n’est pas déjà libérée.</span><span class="sxs-lookup"><span data-stu-id="5ca23-118">Free string if not already freed.</span></span>                                     |
| <span data-ttu-id="5ca23-119">**ReallocProvStr**</span><span class="sxs-lookup"><span data-stu-id="5ca23-119">**ReallocProvStr**</span></span>  | <span data-ttu-id="5ca23-120">Allouez de la mémoire contiguë.</span><span class="sxs-lookup"><span data-stu-id="5ca23-120">Allocate contiguous memory.</span></span>                                           |
| <span data-ttu-id="5ca23-121">**ProvAllocString**</span><span class="sxs-lookup"><span data-stu-id="5ca23-121">**ProvAllocString**</span></span> | <span data-ttu-id="5ca23-122">Vérifie la chaîne et le premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="5ca23-122">Verifies string and first parameter.</span></span> <span data-ttu-id="5ca23-123">Si c’est le cas, effectue l’allocation.</span><span class="sxs-lookup"><span data-stu-id="5ca23-123">If OK, then performs allocation.</span></span> |



 

 

 




