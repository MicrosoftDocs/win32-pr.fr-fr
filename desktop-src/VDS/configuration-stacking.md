---
description: Empilement de configurations
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: Empilement de configurations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50b90629556b5ed00db712b49fe8fa4e48ea8cc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104561300"
---
# <a name="configuration-stacking"></a><span data-ttu-id="a0391-103">Empilement de configurations</span><span class="sxs-lookup"><span data-stu-id="a0391-103">Configuration Stacking</span></span>

<span data-ttu-id="a0391-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a0391-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="a0391-105">L’empilement implique la concaténation d’un ensemble de mappages de blocs logiques.</span><span class="sxs-lookup"><span data-stu-id="a0391-105">Stacking involves the concatenating of a set of logical block mappings.</span></span> <span data-ttu-id="a0391-106">Vous pouvez empiler plusieurs numéros d’unités logiques à partir du même sous-système sous un même numéro d’unité logique.</span><span class="sxs-lookup"><span data-stu-id="a0391-106">You can stack multiple LUNs from the same subsystem under one LUN.</span></span> <span data-ttu-id="a0391-107">Vous pouvez empiler un numéro d’unité logique avec des volumes à partir du même Pack sous un seul volume.</span><span class="sxs-lookup"><span data-stu-id="a0391-107">You can stack a LUN together with volumes from the same pack under one volume.</span></span> <span data-ttu-id="a0391-108">En outre, vous pouvez empiler plusieurs numéros d’unités logiques qui sont exposés par des sous-systèmes hétérogènes sous un seul volume.</span><span class="sxs-lookup"><span data-stu-id="a0391-108">Further, you can stack multiple LUNs that are surfaced by heterogeneous subsystems under one volume.</span></span>

<span data-ttu-id="a0391-109">Comme le montre l’illustration suivante, la création d’un volume ne change pas la liaison existante d’un numéro d’unité logique contributeur.</span><span class="sxs-lookup"><span data-stu-id="a0391-109">As the following illustration shows, the creating of a volume does not change the existing binding of a contributing LUN.</span></span> <span data-ttu-id="a0391-110">De même, l’annulation de la liaison d’un volume ne dissocie pas un LUN contributeur.</span><span class="sxs-lookup"><span data-stu-id="a0391-110">Similarly, the unbinding of a volume does not unbind a contributing LUN.</span></span> <span data-ttu-id="a0391-111">L’illustration représente la configuration RAID 0 1 (0 + 1).</span><span class="sxs-lookup"><span data-stu-id="a0391-111">The illustration depicts the RAID 0 1 (0+1) configuration.</span></span> <span data-ttu-id="a0391-112">Cette configuration connue combine l’entrelacement (RAID 0) et la mise en miroir (RAID 1), qui associe l’accès rapide aux données de RAID 0 à la fiabilité de RAID 1.</span><span class="sxs-lookup"><span data-stu-id="a0391-112">This well-known configuration combines striping (RAID 0) and mirroring (RAID 1), which pairs the fast data access of RAID 0 with the reliability of RAID 1.</span></span>

![Diagramme illustrant une configuration RAID 0 1 (0 + 1).](images/vdsstacklunvolzeroplusone.png)

<span data-ttu-id="a0391-114">La contribution des numéros d’unités logiques peut avoir des types de liaison différents.</span><span class="sxs-lookup"><span data-stu-id="a0391-114">Contributing LUNs can have different binding types.</span></span> <span data-ttu-id="a0391-115">De nombreuses configurations sont possibles avec VDS, mais sont très peu probables, comme dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="a0391-115">Many configurations are possible with VDS but are highly unlikely, such as the next illustration.</span></span> <span data-ttu-id="a0391-116">Dans cet exemple, un plex de volume est un numéro d’unité logique agrégé par bandes et l’autre est un numéro d’unité logique (LUN) en miroir triple.</span><span class="sxs-lookup"><span data-stu-id="a0391-116">In this example, one volume plex is a striped LUN and the other is a three-way mirrored LUN.</span></span>

![Diagramme illustrant une configuration VDS dans laquelle un plex de volume est un LUN agrégé par bandes et l’autre est un numéro d’unité logique (LUN) en miroir 3 voies.](images/vdsstacklunvol.png)

<span data-ttu-id="a0391-118">Bien qu’il ne soit pas pratique, cet exemple illustre un aspect important de l’empilement.</span><span class="sxs-lookup"><span data-stu-id="a0391-118">Although impractical, this example illustrates an important aspect of stacking.</span></span> <span data-ttu-id="a0391-119">Étant donné que l’empilement concatène les plex, VDS ajoute les trois Plex LUN aux deux plex de volume pour un total de cinq Plex.</span><span class="sxs-lookup"><span data-stu-id="a0391-119">Because stacking concatenates plexes, VDS adds the three LUN plexes to the two volume plexes for a total of five plexes.</span></span>

 

 
