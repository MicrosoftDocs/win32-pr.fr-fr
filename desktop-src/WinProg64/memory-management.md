---
title: Gestion de la mémoire sous WOW64
description: La gestion de la mémoire sous WOW64 dépend de l’architecture du processeur.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- WOW64 64 bits, gestion de la mémoire
- gestion de la mémoire 64 bits (programmation Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8602bf6e7e7d9e55894215938932559cfadc6848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382583"
---
# <a name="memory-management-under-wow64"></a><span data-ttu-id="93061-105">Gestion de la mémoire sous WOW64</span><span class="sxs-lookup"><span data-stu-id="93061-105">Memory Management Under WOW64</span></span>

<span data-ttu-id="93061-106">La gestion de la mémoire sous WOW64 dépend de l’architecture du processeur.</span><span class="sxs-lookup"><span data-stu-id="93061-106">Memory management under WOW64 depends on the processor architecture.</span></span>

## <a name="itanium-support"></a><span data-ttu-id="93061-107">Prise en charge d’Itanium</span><span class="sxs-lookup"><span data-stu-id="93061-107">Itanium Support</span></span>

<span data-ttu-id="93061-108">WOW64 simule des pages de 4 Ko en plus des pages natives de 8 Ko que le processeur Itanium utilise.</span><span class="sxs-lookup"><span data-stu-id="93061-108">WOW64 simulates 4 KB pages on top of the native 8 KB pages that the Itanium processor uses.</span></span> <span data-ttu-id="93061-109">Le processeur vous aide en fournissant une excellente simulation avec une faible surcharge.</span><span class="sxs-lookup"><span data-stu-id="93061-109">The processor assists by providing excellent simulation with low overhead.</span></span> <span data-ttu-id="93061-110">Le code de simulation ne peut pas gérer les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="93061-110">The simulation code cannot handle the following cases:</span></span>

-   <span data-ttu-id="93061-111">Suivi des écritures.</span><span class="sxs-lookup"><span data-stu-id="93061-111">Write tracking.</span></span> <span data-ttu-id="93061-112">Les fonctions [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) et [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) sont implémentées dans le noyau à l’aide de la granularité de taille de page native, ce qui signifie que la simulation de page WOW64 4 Ko ne peut pas déterminer les pages de 4 Ko simulées qui sont écrites dans la page de 8 Ko sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="93061-112">The [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) and [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) functions are implemented in the kernel using native page-size granularity, which means the WOW64 4 KB page simulation cannot determine which simulated 4 KB pages are written within the underlying 8 KB page.</span></span>
-   <span data-ttu-id="93061-113">[AWE (Address Windowing Extensions)](/windows/desktop/Memory/address-windowing-extensions).</span><span class="sxs-lookup"><span data-stu-id="93061-113">[Address Windowing Extensions (AWE)](/windows/desktop/Memory/address-windowing-extensions).</span></span> <span data-ttu-id="93061-114">Les fonctions AWE fonctionnent sur les numéros de page et il n’existe aucun moyen de mapper les numéros de page 64 bits sur les numéros de page 32 bits.</span><span class="sxs-lookup"><span data-stu-id="93061-114">The AWE functions operate on page numbers, and there is no way to map 64-bit page numbers to 32-bit page numbers.</span></span>
-   <span data-ttu-id="93061-115">Alignement des sections.</span><span class="sxs-lookup"><span data-stu-id="93061-115">Section alignment.</span></span> <span data-ttu-id="93061-116">Pour les images exécutables avec un alignement de section inférieur à 8 Ko (la valeur par défaut est 4 Ko pour les images x86), WOW64 doit incorrectiser toutes les pages d’image.</span><span class="sxs-lookup"><span data-stu-id="93061-116">For executable images with section alignment smaller than 8 KB (the default is 4 KB for x86 images), WOW64 must dirty all image pages.</span></span> <span data-ttu-id="93061-117">Cela copie efficacement chaque page dans le fichier d’échange et empêche le partage des pages d’images en lecture seule entre les processus.</span><span class="sxs-lookup"><span data-stu-id="93061-117">This effectively copies each page to the page file, and prevents read-only image pages from being shared between processes.</span></span>
-   <span data-ttu-id="93061-118">Les fonctions [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) et [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="93061-118">The [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) functions are not supported.</span></span>

## <a name="x64-and-arm64-support"></a><span data-ttu-id="93061-119">Prise en charge x64 et ARM64</span><span class="sxs-lookup"><span data-stu-id="93061-119">x64 and ARM64 Support</span></span>

<span data-ttu-id="93061-120">La taille de page native est de 4 Ko.</span><span class="sxs-lookup"><span data-stu-id="93061-120">The native page size is 4 KB.</span></span> <span data-ttu-id="93061-121">Par conséquent, les éléments suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="93061-121">Therefore, the following are supported:</span></span>

-   <span data-ttu-id="93061-122">Les fonctions [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) et [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="93061-122">The [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) and [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) functions are supported.</span></span>
-   <span data-ttu-id="93061-123">Les fonctions [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) et [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="93061-123">The [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) functions are supported.</span></span>
-   <span data-ttu-id="93061-124">L’utilisation d’adresses volumineuses présente des avantages, car x64 WOW64 prend en charge un espace d’adressage virtuel de 4 Go.</span><span class="sxs-lookup"><span data-stu-id="93061-124">There are advantages to using large addresses because x64 WOW64 supports a 4 GB virtual address space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93061-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="93061-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93061-126">Limites de mémoire pour les versions de Windows</span><span class="sxs-lookup"><span data-stu-id="93061-126">Memory Limits for Windows Releases</span></span>](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[<span data-ttu-id="93061-127">Réglage de RAM 4GT</span><span class="sxs-lookup"><span data-stu-id="93061-127">4GT RAM Tuning</span></span>](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 