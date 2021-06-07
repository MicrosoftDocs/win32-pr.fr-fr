---
description: La plage de travail d’un programme est une collection de ces pages dans son espace d’adressage virtuel qui ont été récemment référencées.
ms.assetid: 6017ef59-d2e9-4245-a406-8965024dbb35
title: Traiter la plage de travail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaded3d0b5f8c6ad552cc728c68ad0407391c343
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549901"
---
# <a name="process-working-set"></a><span data-ttu-id="945ee-103">Traiter la plage de travail</span><span class="sxs-lookup"><span data-stu-id="945ee-103">Process Working Set</span></span>

<span data-ttu-id="945ee-104">La *plage de travail* d’un programme est une collection de ces pages dans son espace d’adressage virtuel qui ont été récemment référencées.</span><span class="sxs-lookup"><span data-stu-id="945ee-104">The *working set* of a program is a collection of those pages in its virtual address space that have been recently referenced.</span></span> <span data-ttu-id="945ee-105">Il comprend des données partagées et privées.</span><span class="sxs-lookup"><span data-stu-id="945ee-105">It includes both shared and private data.</span></span> <span data-ttu-id="945ee-106">Les données partagées incluent des pages qui contiennent toutes les instructions exécutées par votre application, y compris celles qui figurent dans vos dll et les DLL système.</span><span class="sxs-lookup"><span data-stu-id="945ee-106">The shared data includes pages that contain all instructions your application executes, including those in your DLLs and the system DLLs.</span></span> <span data-ttu-id="945ee-107">À mesure que la taille de la plage de travail augmente, la demande de mémoire augmente.</span><span class="sxs-lookup"><span data-stu-id="945ee-107">As the working set size increases, memory demand increases.</span></span>

<span data-ttu-id="945ee-108">Un processus est associé à une taille de jeu de travail minimale et à une taille de jeu de travail maximale.</span><span class="sxs-lookup"><span data-stu-id="945ee-108">A process has an associated minimum working set size and maximum working set size.</span></span> <span data-ttu-id="945ee-109">Chaque fois que vous appelez [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), il réserve la taille minimale du jeu de travail pour le processus.</span><span class="sxs-lookup"><span data-stu-id="945ee-109">Each time you call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), it reserves the minimum working set size for the process.</span></span> <span data-ttu-id="945ee-110">Le gestionnaire de mémoire virtuelle tente de conserver suffisamment de mémoire pour la plage de travail minimale résidant lorsque le processus est actif, mais ne conserve pas plus de la taille maximale.</span><span class="sxs-lookup"><span data-stu-id="945ee-110">The virtual memory manager attempts to keep enough memory for the minimum working set resident when the process is active, but keeps no more than the maximum size.</span></span>

<span data-ttu-id="945ee-111">Pour obtenir les tailles minimale et maximale requises de la plage de travail de votre application, appelez la fonction [**GetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize) .</span><span class="sxs-lookup"><span data-stu-id="945ee-111">To get the requested minimum and maximum sizes of the working set for your application, call the [**GetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-getprocessworkingsetsize) function.</span></span>

<span data-ttu-id="945ee-112">Le système définit les tailles de la plage de travail par défaut.</span><span class="sxs-lookup"><span data-stu-id="945ee-112">The system sets the default working set sizes.</span></span> <span data-ttu-id="945ee-113">Vous pouvez également modifier les tailles de la plage de travail à l’aide de la fonction [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) .</span><span class="sxs-lookup"><span data-stu-id="945ee-113">You can also modify the working set sizes using the [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) function.</span></span> <span data-ttu-id="945ee-114">La définition de ces valeurs n’est pas une garantie que la mémoire sera réservée ou résidera.</span><span class="sxs-lookup"><span data-stu-id="945ee-114">Setting these values is not a guarantee that the memory will be reserved or resident.</span></span> <span data-ttu-id="945ee-115">Soyez prudent lorsque vous demandez une taille de jeu de travail minimale ou maximale, car cela peut nuire aux performances du système.</span><span class="sxs-lookup"><span data-stu-id="945ee-115">Be careful about requesting too large a minimum or maximum working set size, because doing so can degrade system performance.</span></span>

<span data-ttu-id="945ee-116">Pour obtenir la taille actuelle ou maximale de la plage de travail de votre processus, utilisez la fonction [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) .</span><span class="sxs-lookup"><span data-stu-id="945ee-116">To obtain the current or peak size of the working set for your process, use the [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="945ee-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="945ee-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="945ee-118">[Informations sur les performances de la mémoire](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="945ee-118">[Memory Performance Information](/previous-versions/windows/desktop/legacy/aa965225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="945ee-119">Plage de travail</span><span class="sxs-lookup"><span data-stu-id="945ee-119">Working Set</span></span>](../memory/working-set.md)
</dt> </dl>

 

 
