---
title: Informations sur l’utilisation de la mémoire du processus
description: La fonction GetProcessMemoryInfo prend un handle de processus comme entrée et remplit une structure de compteurs de mémoire de processus \_ \_ avec des informations sur les statistiques de mémoire pour le processus.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133032b8cfb8a9af4ccea5661c9e0e0181ab4d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840490"
---
# <a name="process-memory-usage-information"></a><span data-ttu-id="76a0b-103">Informations sur l’utilisation de la mémoire du processus</span><span class="sxs-lookup"><span data-stu-id="76a0b-103">Process Memory Usage Information</span></span>

<span data-ttu-id="76a0b-104">La fonction [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) prend un handle de processus comme entrée et remplit une structure de [**\_ \_ compteurs de mémoire de processus**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) avec des informations sur les statistiques de mémoire pour le processus.</span><span class="sxs-lookup"><span data-stu-id="76a0b-104">The [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) function takes a process handle as input and fills a [**PROCESS\_MEMORY\_COUNTERS**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) structure with information about the memory statistics for the process.</span></span> <span data-ttu-id="76a0b-105">Le membre **CB** reçoit la taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="76a0b-105">The **cb** member receives the size of the structure.</span></span> <span data-ttu-id="76a0b-106">Le membre **PageFaultCount** reçoit le nombre de défauts de page.</span><span class="sxs-lookup"><span data-stu-id="76a0b-106">The **PageFaultCount** member receives the number of page faults.</span></span> <span data-ttu-id="76a0b-107">Les membres restants reçoivent l’utilisation actuelle et maximale de la mémoire dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="76a0b-107">The remaining members receive the current and peak memory usage in the following categories:</span></span>

-   <span data-ttu-id="76a0b-108">Plage de travail</span><span class="sxs-lookup"><span data-stu-id="76a0b-108">working set</span></span>
-   <span data-ttu-id="76a0b-109">pool paginé</span><span class="sxs-lookup"><span data-stu-id="76a0b-109">paged pool</span></span>
-   <span data-ttu-id="76a0b-110">pool non paginé</span><span class="sxs-lookup"><span data-stu-id="76a0b-110">nonpaged pool</span></span>
-   <span data-ttu-id="76a0b-111">fichier</span><span class="sxs-lookup"><span data-stu-id="76a0b-111">pagefile</span></span>

<span data-ttu-id="76a0b-112">La *plage de travail* correspond à la quantité de mémoire physiquement mappée au contexte de processus à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="76a0b-112">The *working set* is the amount of memory physically mapped to the process context at a given time.</span></span> <span data-ttu-id="76a0b-113">La mémoire de la *réserve paginée* est la mémoire système qui peut être transférée vers le fichier d’échange sur le disque (paginée) lorsqu’elle n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="76a0b-113">Memory in the *paged pool* is system memory that can be transferred to the paging file on disk (paged) when it is not being used.</span></span> <span data-ttu-id="76a0b-114">La mémoire dans la *réserve non paginée* est une mémoire système qui ne peut pas être paginée sur le disque tant que les objets correspondants sont alloués.</span><span class="sxs-lookup"><span data-stu-id="76a0b-114">Memory in the *nonpaged pool* is system memory that cannot be paged to disk as long as the corresponding objects are allocated.</span></span> <span data-ttu-id="76a0b-115">L' *utilisation du fichier d’échange représente* la quantité de mémoire réservée pour le processus dans le fichier de pagination système.</span><span class="sxs-lookup"><span data-stu-id="76a0b-115">The *pagefile* usage represents how much memory is set aside for the process in the system paging file.</span></span> <span data-ttu-id="76a0b-116">Lorsque l’utilisation de la mémoire est trop élevée, les pages du gestionnaire de mémoire virtuelle ont sélectionné la mémoire sur le disque.</span><span class="sxs-lookup"><span data-stu-id="76a0b-116">When memory usage is too high, the virtual memory manager pages selected memory to disk.</span></span> <span data-ttu-id="76a0b-117">Quand un thread a besoin d’une page qui n’est pas dans la mémoire, le gestionnaire de mémoire le recharge à partir du fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="76a0b-117">When a thread needs a page that is not in memory, the memory manager reloads it from the paging file.</span></span>

 

 




