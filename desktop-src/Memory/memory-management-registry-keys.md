---
description: L’espace d’adressage virtuel du système (VA) sur les systèmes 32 bits peut devenir épuisé en raison de la fragmentation. Plusieurs clés de Registre peuvent être utilisées pour configurer les limites de mémoire sur les systèmes 32 bits qui rencontrent ce problème.
ms.assetid: ec2a8c6b-cd8e-4085-b337-02f78a210bb5
title: Clés de registre de gestion de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e8c53bd54f8caeb82aad58ceed61cc5644c112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869065"
---
# <a name="memory-management-registry-keys"></a><span data-ttu-id="8785f-104">Clés de registre de gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="8785f-104">Memory Management Registry Keys</span></span>

<span data-ttu-id="8785f-105">L’espace d’adressage virtuel du système (VA) sur les systèmes 32 bits peut devenir épuisé en raison de la fragmentation.</span><span class="sxs-lookup"><span data-stu-id="8785f-105">System virtual address (VA) space on 32-bit systems can become exhausted due to fragmentation.</span></span> <span data-ttu-id="8785f-106">Plusieurs clés de Registre peuvent être utilisées pour configurer les limites de mémoire sur les systèmes 32 bits qui rencontrent ce problème.</span><span class="sxs-lookup"><span data-stu-id="8785f-106">Several registry keys can be used to configure memory limits on 32-bit systems that experience this issue.</span></span> <span data-ttu-id="8785f-107">L’espace système VA sur les systèmes 64 bits n’est pas soumis à l’épuisement par fragmentation ; par conséquent, ces clés n’ont aucun effet sur les systèmes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8785f-107">System VA space on 64-bit systems is not subject to exhaustion by fragmentation; therefore, these keys have no effect on 64-bit systems.</span></span>

<span data-ttu-id="8785f-108">Pour les systèmes 32 bits, ces clés de registre de gestion de la mémoire doivent être créées explicitement sous la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="8785f-108">For 32-bit systems, these memory management registry keys must be explicitly created under the following registry key:</span></span>

<span data-ttu-id="8785f-109">**HKEY \_ \_** Contrôle actuel du jeu de \\  \\ **contrôle** de \\  \\ **session** \\  du système d’ordinateur local gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="8785f-109">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**Current Control Set**\\**Control**\\**Session Manager**\\**Memory Management**</span></span>

<span data-ttu-id="8785f-110">**Windows Server 2008 et Windows Vista :** Ces clés de Registre sont disponibles sur les systèmes 32 bits à partir de Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="8785f-110">**Windows Server 2008 and Windows Vista:** These registry keys are available on 32-bit systems starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="8785f-111">Pour les limites de mémoire et d’espace d’adressage par défaut sur les systèmes 32 bits et 64 bits, consultez [limites de mémoire pour les versions de Windows](memory-limits-for-windows-releases.md).</span><span class="sxs-lookup"><span data-stu-id="8785f-111">For default memory and address space limits on both 32-bit and 64-bit systems, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span>

<span data-ttu-id="8785f-112">Le tableau suivant décrit les clés de registre de gestion de la mémoire qui peuvent être utilisées pour configurer les limites de mémoire sur les systèmes 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8785f-112">The following table describes the memory management registry keys that can be used to configure memory limits on 32-bit systems.</span></span> <span data-ttu-id="8785f-113">Toutes ces clés ont un \_ type DWORD reg et les valeurs possibles sont comprises entre 0 et 2 048 Mo.</span><span class="sxs-lookup"><span data-stu-id="8785f-113">All of these keys have a REG\_DWORD type and possible values that range from 0 through 2,048 MB.</span></span> <span data-ttu-id="8785f-114">La valeur par défaut est 0, ce qui signifie qu’aucune limite n’est appliquée.</span><span class="sxs-lookup"><span data-stu-id="8785f-114">The default is 0, which means no limit is enforced.</span></span> <span data-ttu-id="8785f-115">Les valeurs sont automatiquement arrondies à la limite d’allocation de VA du système suivante, qui est de 2 Mo sur les systèmes 32 bits sur lesquels l' [extension d’adresse physique](physical-address-extension.md) (PAE) est activée et 4 Mo sur les systèmes 32 bits sur lesquels PAE n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="8785f-115">Values are automatically rounded up to the next system VA allocation boundary, which is 2 MB on 32-bit systems that have [Physical Address Extension](physical-address-extension.md) (PAE) enabled and 4 MB on 32-bit systems that do not have PAE enabled.</span></span>



| <span data-ttu-id="8785f-116">Clé</span><span class="sxs-lookup"><span data-stu-id="8785f-116">Key</span></span>                   | <span data-ttu-id="8785f-117">Description</span><span class="sxs-lookup"><span data-stu-id="8785f-117">Description</span></span>                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8785f-118">**NonPagedPoolLimit**</span><span class="sxs-lookup"><span data-stu-id="8785f-118">**NonPagedPoolLimit**</span></span> | <span data-ttu-id="8785f-119">Spécifie la quantité maximale d’espace de VA du système qui peut être utilisée par la réserve non paginée.</span><span class="sxs-lookup"><span data-stu-id="8785f-119">Specifies the maximum amount of system VA space that can be used by the nonpaged pool.</span></span> <span data-ttu-id="8785f-120">Dans certaines conditions, cette limite peut être dépassée d’une petite quantité.</span><span class="sxs-lookup"><span data-stu-id="8785f-120">Under certain conditions, this limit may be exceeded by a small amount.</span></span> |
| <span data-ttu-id="8785f-121">**PagedPoolLimit**</span><span class="sxs-lookup"><span data-stu-id="8785f-121">**PagedPoolLimit**</span></span>    | <span data-ttu-id="8785f-122">Spécifie la quantité maximale d’espace de VA du système qui peut être utilisée par la réserve paginée.</span><span class="sxs-lookup"><span data-stu-id="8785f-122">Specifies the maximum amount of system VA space that can be used by the paged pool.</span></span>                                                                            |
| <span data-ttu-id="8785f-123">**SessionSpaceLimit**</span><span class="sxs-lookup"><span data-stu-id="8785f-123">**SessionSpaceLimit**</span></span> | <span data-ttu-id="8785f-124">Spécifie la quantité maximale d’espace de VA du système qui peut être utilisée par les allocations d’espace de session.</span><span class="sxs-lookup"><span data-stu-id="8785f-124">Specifies the maximum amount of system VA space that can be used by session space allocations.</span></span>                                                                 |
| <span data-ttu-id="8785f-125">**SystemCacheLimit**</span><span class="sxs-lookup"><span data-stu-id="8785f-125">**SystemCacheLimit**</span></span>  | <span data-ttu-id="8785f-126">Spécifie la quantité maximale d’espace de VA du système qui peut être utilisée par le cache système.</span><span class="sxs-lookup"><span data-stu-id="8785f-126">Specifies the maximum amount of system VA space that can be used by the system cache.</span></span> <span data-ttu-id="8785f-127">Dans certaines conditions, cette limite peut être dépassée d’une petite quantité.</span><span class="sxs-lookup"><span data-stu-id="8785f-127">Under certain conditions, this limit may be exceeded by a small amount.</span></span>  |
| <span data-ttu-id="8785f-128">**SystemPtesLimit**</span><span class="sxs-lookup"><span data-stu-id="8785f-128">**SystemPtesLimit**</span></span>   | <span data-ttu-id="8785f-129">Spécifie la quantité maximale d’espace de VA système qui peut être utilisée par les mappages d’e/s et d’autres ressources qui utilisent des entrées de table de pages système (PTE).</span><span class="sxs-lookup"><span data-stu-id="8785f-129">Specifies the maximum amount of system VA space that can be used by I/O mappings and other resources that consume system page table entries (PTEs).</span></span>            |



 

<span data-ttu-id="8785f-130">L’utilisation d’un débogueur de noyau permet de déterminer si l’espace du système VA être épuisé.</span><span class="sxs-lookup"><span data-stu-id="8785f-130">Determining whether system VA space is being exhausted requires the use of a kernel debugger.</span></span> <span data-ttu-id="8785f-131">Pour plus d'informations, consultez [Outils de débogage pour Windows](https://msdn.microsoft.com/library/cc267445.aspx).</span><span class="sxs-lookup"><span data-stu-id="8785f-131">For more information, see [Debugging Tools for Windows](https://msdn.microsoft.com/library/cc267445.aspx).</span></span>

 

 



