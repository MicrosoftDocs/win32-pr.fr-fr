---
description: Objets de fournisseur de logiciels
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Objets de fournisseur de logiciels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16f81cd975c892760d1851720e65584453e7745
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "103869334"
---
# <a name="software-provider-objects"></a><span data-ttu-id="74687-103">Objets de fournisseur de logiciels</span><span class="sxs-lookup"><span data-stu-id="74687-103">Software Provider Objects</span></span>

<span data-ttu-id="74687-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="74687-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="74687-105">Les objets de fournisseur de logiciels modélisent des appareils physiques, tels que des disques IDE et des CD-ROM, et des éléments virtuels tels que des packs, des volumes et des plex de volume.</span><span class="sxs-lookup"><span data-stu-id="74687-105">Software provider objects model physical devices, such as IDE disks and CD-ROMs, and virtual elements like packs, volumes, and volume plexes.</span></span> <span data-ttu-id="74687-106">L’illustration suivante montre la relation entre l’objet de fournisseur et le jeu d’objets de fournisseur de logiciels, ainsi que la relation entre les différents objets de fournisseur de logiciels eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="74687-106">The following illustration shows the relationship between the provider object and the set of software provider objects, as well as the relationship between the various software provider objects themselves.</span></span>

![Diagramme qui montre la relation entre un « fournisseur » et des objets de fournisseur de logiciels, tels que « Pack » et « volume ».](images/vdsswobjects.png)

<span data-ttu-id="74687-108">Un objet fournisseur peut contenir zéro ou plusieurs packs.</span><span class="sxs-lookup"><span data-stu-id="74687-108">A provider object can contain zero or more packs.</span></span> <span data-ttu-id="74687-109">Un objet Pack peut contenir zéro, un ou plusieurs disques et volumes.</span><span class="sxs-lookup"><span data-stu-id="74687-109">A pack object can contain zero or more disks and volumes.</span></span> <span data-ttu-id="74687-110">Un volume comprend au moins un plex de volume et chaque plex de volume peut être mappé à un ou plusieurs disques, selon le type de plex.</span><span class="sxs-lookup"><span data-stu-id="74687-110">A volume comprises of at least one volume plex and each volume plex can map to one or more disks, depending on the plex type.</span></span> <span data-ttu-id="74687-111">VDS gère directement les disques non alloués, sans conteneur de packs.</span><span class="sxs-lookup"><span data-stu-id="74687-111">VDS manages unallocated disks directly, without a pack container.</span></span> <span data-ttu-id="74687-112">Les autres rubriques de cette section décrivent les objets Pack, disque, volume et Plex volume.</span><span class="sxs-lookup"><span data-stu-id="74687-112">The remaining topics of this section describe the pack, disk, volume, and volume plex objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74687-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="74687-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74687-114">Modèle d’objet VDS</span><span class="sxs-lookup"><span data-stu-id="74687-114">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
