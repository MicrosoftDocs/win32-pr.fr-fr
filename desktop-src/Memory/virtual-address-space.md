---
description: L’espace d’adressage virtuel d’un processus correspond à l’ensemble des adresses mémoire virtuelles qu’il peut utiliser. L’espace d’adressage de chaque processus est privé et n’est pas accessible par d’autres processus, sauf s’il est partagé.
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: Espace d’adressage virtuel (gestion de la mémoire)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6584d0404799e6b0e5ab343c7d8b39d7f8d741a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951331"
---
# <a name="virtual-address-space-memory-management"></a><span data-ttu-id="228df-104">Espace d’adressage virtuel (gestion de la mémoire)</span><span class="sxs-lookup"><span data-stu-id="228df-104">Virtual Address Space (Memory Management)</span></span>

<span data-ttu-id="228df-105">L’espace d’adressage virtuel d’un processus correspond à l’ensemble des adresses mémoire virtuelles qu’il peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="228df-105">The virtual address space for a process is the set of virtual memory addresses that it can use.</span></span> <span data-ttu-id="228df-106">L’espace d’adressage de chaque processus est privé et n’est pas accessible par d’autres processus, sauf s’il est partagé.</span><span class="sxs-lookup"><span data-stu-id="228df-106">The address space for each process is private and cannot be accessed by other processes unless it is shared.</span></span>

<span data-ttu-id="228df-107">Une adresse virtuelle ne représente pas l’emplacement physique réel d’un objet en mémoire ; au lieu de cela, le système gère une *table de pages* pour chaque processus, qui est une structure de données interne utilisée pour convertir des adresses virtuelles en adresses physiques correspondantes.</span><span class="sxs-lookup"><span data-stu-id="228df-107">A virtual address does not represent the actual physical location of an object in memory; instead, the system maintains a *page table* for each process, which is an internal data structure used to translate virtual addresses into their corresponding physical addresses.</span></span> <span data-ttu-id="228df-108">Chaque fois qu’un thread fait référence à une adresse, le système convertit l’adresse virtuelle en adresse physique.</span><span class="sxs-lookup"><span data-stu-id="228df-108">Each time a thread references an address, the system translates the virtual address to a physical address.</span></span>

<span data-ttu-id="228df-109">L’espace d’adressage virtuel pour Windows 32 bits a une taille de 4 gigaoctets (Go) et est divisé en deux partitions : une pour une utilisation par le processus et l’autre réservée pour une utilisation par le système.</span><span class="sxs-lookup"><span data-stu-id="228df-109">The virtual address space for 32-bit Windows is 4 gigabytes (GB) in size and divided into two partitions: one for use by the process and the other reserved for use by the system.</span></span> <span data-ttu-id="228df-110">Pour plus d’informations sur l’espace d’adressage virtuel dans Windows 64 bits, consultez [espace d’adressage virtuel dans windows 64 bits](../winprog64/virtual-address-space.md).</span><span class="sxs-lookup"><span data-stu-id="228df-110">For more information about the virtual address space in 64-bit Windows, see [Virtual Address Space in 64-bit Windows](../winprog64/virtual-address-space.md).</span></span>

<span data-ttu-id="228df-111">Pour plus d’informations sur la mémoire virtuelle, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="228df-111">For more information about virtual memory, see the following topics:</span></span>

-   [<span data-ttu-id="228df-112">Espace d’adressage virtuel et stockage physique</span><span class="sxs-lookup"><span data-stu-id="228df-112">Virtual Address Space and Physical Storage</span></span>](virtual-address-space-and-physical-storage.md)
-   [<span data-ttu-id="228df-113">Plage de travail</span><span class="sxs-lookup"><span data-stu-id="228df-113">Working Set</span></span>](working-set.md)
-   [<span data-ttu-id="228df-114">État de la page</span><span class="sxs-lookup"><span data-stu-id="228df-114">Page State</span></span>](page-state.md)
-   [<span data-ttu-id="228df-115">Portée de la mémoire allouée</span><span class="sxs-lookup"><span data-stu-id="228df-115">Scope of Allocated Memory</span></span>](scope-of-allocated-memory.md)
-   [<span data-ttu-id="228df-116">Prévention de l’exécution des données</span><span class="sxs-lookup"><span data-stu-id="228df-116">Data Execution Prevention</span></span>](data-execution-prevention.md)
-   [<span data-ttu-id="228df-117">Protection de la mémoire</span><span class="sxs-lookup"><span data-stu-id="228df-117">Memory Protection</span></span>](memory-protection.md)
-   [<span data-ttu-id="228df-118">Limites de mémoire pour les versions de Windows</span><span class="sxs-lookup"><span data-stu-id="228df-118">Memory Limits for Windows Releases</span></span>](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a><span data-ttu-id="228df-119">Espace d’adressage virtuel par défaut pour Windows 32 bits</span><span class="sxs-lookup"><span data-stu-id="228df-119">Default Virtual Address Space for 32-bit Windows</span></span>

<span data-ttu-id="228df-120">Le tableau suivant indique la plage de mémoire par défaut pour chaque partition.</span><span class="sxs-lookup"><span data-stu-id="228df-120">The following table shows the default memory range for each partition.</span></span>



| <span data-ttu-id="228df-121">Plage mémoire</span><span class="sxs-lookup"><span data-stu-id="228df-121">Memory range</span></span>                             | <span data-ttu-id="228df-122">Utilisation</span><span class="sxs-lookup"><span data-stu-id="228df-122">Usage</span></span>                |
|------------------------------------------|----------------------|
| <span data-ttu-id="228df-123">2 Go bas (0x00000000 à 0x7FFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="228df-123">Low 2GB (0x00000000 through 0x7FFFFFFF)</span></span>  | <span data-ttu-id="228df-124">Utilisé par le processus.</span><span class="sxs-lookup"><span data-stu-id="228df-124">Used by the process.</span></span> |
| <span data-ttu-id="228df-125">2 Go de poids fort (0x80000000 à 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="228df-125">High 2GB (0x80000000 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="228df-126">Utilisé par le système.</span><span class="sxs-lookup"><span data-stu-id="228df-126">Used by the system.</span></span>  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a><span data-ttu-id="228df-127">Espace d’adressage virtuel pour Windows 32 bits avec 4GT</span><span class="sxs-lookup"><span data-stu-id="228df-127">Virtual Address Space for 32-bit Windows with 4GT</span></span>

<span data-ttu-id="228df-128">Si le [réglage à 4 gigaoctets](4-gigabyte-tuning.md) (4GT) est activé, la plage de mémoire pour chaque partition est la suivante.</span><span class="sxs-lookup"><span data-stu-id="228df-128">If [4-gigabyte tuning](4-gigabyte-tuning.md) (4GT) is enabled, the memory range for each partition is as follows.</span></span>



| <span data-ttu-id="228df-129">Plage mémoire</span><span class="sxs-lookup"><span data-stu-id="228df-129">Memory range</span></span>                             | <span data-ttu-id="228df-130">Utilisation</span><span class="sxs-lookup"><span data-stu-id="228df-130">Usage</span></span>                |
|------------------------------------------|----------------------|
| <span data-ttu-id="228df-131">3 Go bas (0x00000000 à 0xBFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="228df-131">Low 3GB (0x00000000 through 0xBFFFFFFF)</span></span>  | <span data-ttu-id="228df-132">Utilisé par le processus.</span><span class="sxs-lookup"><span data-stu-id="228df-132">Used by the process.</span></span> |
| <span data-ttu-id="228df-133">Haute de 1 Go (0xC0000000 à 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="228df-133">High 1GB (0xC0000000 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="228df-134">Utilisé par le système.</span><span class="sxs-lookup"><span data-stu-id="228df-134">Used by the system.</span></span>  |



 

<span data-ttu-id="228df-135">Une fois 4GT activé, un processus dont l’en-tête de prise en [**\_ \_ \_ \_ charge d’adresse de fichier image**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) est défini dans son en-tête d’image aura accès aux 1 Go supplémentaires de mémoire au-dessus des 2 Go de basse.</span><span class="sxs-lookup"><span data-stu-id="228df-135">After 4GT is enabled, a process that has the [**IMAGE\_FILE\_LARGE\_ADDRESS\_AWARE**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) flag set in its image header will have access to the additional 1 GB of memory above the low 2 GB.</span></span>

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a><span data-ttu-id="228df-136">Ajustement de l’espace d’adressage virtuel pour Windows 32 bits</span><span class="sxs-lookup"><span data-stu-id="228df-136">Adjusting the Virtual Address Space for 32-bit Windows</span></span>

<span data-ttu-id="228df-137">Vous pouvez utiliser la commande suivante pour définir une option d’entrée de démarrage qui configure la taille de la partition qui peut être utilisée par le processus sur une valeur comprise entre 2048 (2 Go) et 3072 (3 Go) :</span><span class="sxs-lookup"><span data-stu-id="228df-137">You can use the following command to set a boot entry option that configures the size of the partition that is available for use by the process to a value between 2048 (2 GB) and 3072 (3 GB):</span></span>

<span data-ttu-id="228df-138">[Bcdedit/set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *mégaoctets*</span><span class="sxs-lookup"><span data-stu-id="228df-138">[BCDEdit /set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *Megabytes*</span></span>

<span data-ttu-id="228df-139">Une fois l’option d’entrée de démarrage définie, la plage de mémoire pour chaque partition est la suivante.</span><span class="sxs-lookup"><span data-stu-id="228df-139">After the boot entry option is set, the memory range for each partition is as follows.</span></span>



| <span data-ttu-id="228df-140">Plage mémoire</span><span class="sxs-lookup"><span data-stu-id="228df-140">Memory range</span></span>                            | <span data-ttu-id="228df-141">Utilisation</span><span class="sxs-lookup"><span data-stu-id="228df-141">Usage</span></span>                |
|-----------------------------------------|----------------------|
| <span data-ttu-id="228df-142">Faible (0x00000000 à *mégaoctets*)</span><span class="sxs-lookup"><span data-stu-id="228df-142">Low (0x00000000 through *Megabytes*)</span></span>    | <span data-ttu-id="228df-143">Utilisé par le processus.</span><span class="sxs-lookup"><span data-stu-id="228df-143">Used by the process.</span></span> |
| <span data-ttu-id="228df-144">Élevé (*mégaoctets*+ 1 à 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="228df-144">High (*Megabytes*+1 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="228df-145">Utilisé par le système.</span><span class="sxs-lookup"><span data-stu-id="228df-145">Used by the system.</span></span>  |



 

<span data-ttu-id="228df-146">**Windows Server 2003 :** Définissez le commutateur **/USERVA** dans boot.ini sur une valeur comprise entre 2048 et 3072.</span><span class="sxs-lookup"><span data-stu-id="228df-146">**Windows Server 2003:** Set the **/USERVA** switch in boot.ini to a value between 2048 and 3072.</span></span>

 

 
