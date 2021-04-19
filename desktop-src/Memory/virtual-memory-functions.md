---
description: Les fonctions de mémoire virtuelle permettent à un processus de manipuler ou de déterminer l’état des pages dans son espace d’adressage virtuel.
ms.assetid: 9488a854-1ef0-488f-b3d1-57c1acb82a88
title: Fonctions de mémoire virtuelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76866fd10dac01315622e8a4faef7bea436a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517313"
---
# <a name="virtual-memory-functions"></a><span data-ttu-id="30874-103">Fonctions de mémoire virtuelle</span><span class="sxs-lookup"><span data-stu-id="30874-103">Virtual Memory Functions</span></span>

<span data-ttu-id="30874-104">Les fonctions de mémoire virtuelle permettent à un processus de manipuler ou de déterminer l’état des pages dans son espace d’adressage virtuel.</span><span class="sxs-lookup"><span data-stu-id="30874-104">The virtual memory functions enable a process to manipulate or determine the status of pages in its virtual address space.</span></span> <span data-ttu-id="30874-105">Ils peuvent effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="30874-105">They can perform the following operations:</span></span>

-   <span data-ttu-id="30874-106">Réserver une plage de l’espace d’adressage virtuel d’un processus.</span><span class="sxs-lookup"><span data-stu-id="30874-106">Reserve a range of a process's virtual address space.</span></span> <span data-ttu-id="30874-107">La réservation de l’espace d’adressage n’alloue pas de stockage physique, mais empêche d’autres opérations d’allocation d’utiliser la plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="30874-107">Reserving address space does not allocate any physical storage, but it prevents other allocation operations from using the specified range.</span></span> <span data-ttu-id="30874-108">Il n’affecte pas les espaces d’adressage virtuel d’autres processus.</span><span class="sxs-lookup"><span data-stu-id="30874-108">It does not affect the virtual address spaces of other processes.</span></span> <span data-ttu-id="30874-109">La réservation de pages empêche toute consommation inutile de stockage physique, tout en permettant à un processus de réserver une plage de son espace d’adressage dans laquelle une structure de données dynamique peut croître.</span><span class="sxs-lookup"><span data-stu-id="30874-109">Reserving pages prevents needless consumption of physical storage, while enabling a process to reserve a range of its address space into which a dynamic data structure can grow.</span></span> <span data-ttu-id="30874-110">Le processus peut allouer du stockage physique pour cet espace, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="30874-110">The process can allocate physical storage for this space, as needed.</span></span>
-   <span data-ttu-id="30874-111">Validez une plage de pages réservées dans l’espace d’adressage virtuel d’un processus afin que le stockage physique (en RAM ou sur disque) soit accessible uniquement au processus d’allocation.</span><span class="sxs-lookup"><span data-stu-id="30874-111">Commit a range of reserved pages in a process's virtual address space so that physical storage (either in RAM or on disk) is accessible only to the allocating process.</span></span>
-   <span data-ttu-id="30874-112">Spécifiez lecture/écriture, lecture seule ou aucun accès pour une plage de pages validées.</span><span class="sxs-lookup"><span data-stu-id="30874-112">Specify read/write, read-only, or no access for a range of committed pages.</span></span> <span data-ttu-id="30874-113">Cela diffère des fonctions d’allocation standard qui allouent toujours des pages avec un accès en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="30874-113">This differs from the standard allocation functions that always allocate pages with read/write access.</span></span>
-   <span data-ttu-id="30874-114">Libérez une plage de pages réservées, en rendant la plage d’adresses virtuelles disponible pour les opérations d’allocation suivantes par le processus appelant.</span><span class="sxs-lookup"><span data-stu-id="30874-114">Free a range of reserved pages, making the range of virtual addresses available for subsequent allocation operations by the calling process.</span></span>
-   <span data-ttu-id="30874-115">Annulez la validation d’une plage de pages validées, libérez son stockage physique et rendez-la disponible pour une allocation ultérieure par n’importe quel processus.</span><span class="sxs-lookup"><span data-stu-id="30874-115">Decommit a range of committed pages, releasing their physical storage and making it available for subsequent allocation by any process.</span></span>
-   <span data-ttu-id="30874-116">Verrouille une ou plusieurs pages de la mémoire allouée dans la mémoire physique (RAM) afin que le système ne puisse pas échanger les pages dans le fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="30874-116">Lock one or more pages of committed memory into physical memory (RAM) so that the system cannot swap the pages out to the paging file.</span></span>
-   <span data-ttu-id="30874-117">Obtenir des informations sur une plage de pages dans l’espace d’adressage virtuel du processus appelant ou un processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="30874-117">Obtain information about a range of pages in the virtual address space of the calling process or a specified process.</span></span>
-   <span data-ttu-id="30874-118">Modifiez la protection d’accès pour une plage spécifiée de pages validées dans l’espace d’adressage virtuel du processus appelant ou un processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="30874-118">Change the access protection for a specified range of committed pages in the virtual address space of the calling process or a specified process.</span></span>

<span data-ttu-id="30874-119">Pour plus d'informations, consultez les rubriques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="30874-119">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="30874-120">Allocation de mémoire virtuelle</span><span class="sxs-lookup"><span data-stu-id="30874-120">Allocating Virtual Memory</span></span>](allocating-virtual-memory.md)
-   [<span data-ttu-id="30874-121">Comparaison des méthodes d’allocation de mémoire</span><span class="sxs-lookup"><span data-stu-id="30874-121">Comparing Memory Allocation Methods</span></span>](comparing-memory-allocation-methods.md)
-   [<span data-ttu-id="30874-122">Libération de la mémoire virtuelle</span><span class="sxs-lookup"><span data-stu-id="30874-122">Freeing Virtual Memory</span></span>](freeing-virtual-memory.md)
-   [<span data-ttu-id="30874-123">Utilisation des pages</span><span class="sxs-lookup"><span data-stu-id="30874-123">Working With Pages</span></span>](working-with-pages.md)
-   [<span data-ttu-id="30874-124">Fonctions de gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="30874-124">Memory Management Functions</span></span>](memory-management-functions.md)

 

 



