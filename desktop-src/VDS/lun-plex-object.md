---
description: LUN, objet Plex
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: LUN, objet Plex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b51657ccbfc0f1bd3d73e54128cac3f0b507c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535606"
---
# <a name="lun-plex-object"></a><span data-ttu-id="bcb2d-103">LUN, objet Plex</span><span class="sxs-lookup"><span data-stu-id="bcb2d-103">LUN Plex Object</span></span>

<span data-ttu-id="bcb2d-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bcb2d-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="bcb2d-105">Un objet de plex LUN modélise un plex LUN qui est contenu dans un numéro d’unité logique.</span><span class="sxs-lookup"><span data-stu-id="bcb2d-105">A LUN plex object models a LUN plex that is contained by a LUN.</span></span> <span data-ttu-id="bcb2d-106">Seul un numéro d’unité logique en miroir peut avoir plusieurs Plex ; tous les autres types de LUN ont un Plex.</span><span class="sxs-lookup"><span data-stu-id="bcb2d-106">Only a mirrored LUN can have multiple plexes; all other LUN types have one plex.</span></span> <span data-ttu-id="bcb2d-107">Chaque Plex contient une copie des données sur le numéro d’unité logique.</span><span class="sxs-lookup"><span data-stu-id="bcb2d-107">Each plex contains a copy of the data on the LUN.</span></span> <span data-ttu-id="bcb2d-108">De nouveaux Plex peuvent être ajoutés à un numéro d’unité logique (LUN) et, à l’exception du Plex d’origine, les plex existants peuvent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="bcb2d-108">New plexes can be added to a LUN, and, with the exception of the original plex, existing plexes can be removed.</span></span> <span data-ttu-id="bcb2d-109">VDS prend en charge quatre types de plex LUN : simple, fractionné, agrégé par bandes et avec parité.</span><span class="sxs-lookup"><span data-stu-id="bcb2d-109">VDS supports four LUN plex types: simple, spanned, striped, and striped with parity.</span></span> <span data-ttu-id="bcb2d-110">Pour obtenir une description de chacun de ces types de LUN, consultez l' [objet lun](lun-object.md).</span><span class="sxs-lookup"><span data-stu-id="bcb2d-110">For a description of each of these LUN types, see the [LUN Object](lun-object.md).</span></span>

<span data-ttu-id="bcb2d-111">Utilisez la méthode [**IVdsLun :: AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) pour ajouter un Plex à un numéro d’unité logique et la méthode [**IVdsLun :: RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) pour supprimer le plex.</span><span class="sxs-lookup"><span data-stu-id="bcb2d-111">Use the [**IVdsLun::AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) method to add a plex to a LUN and the [**IVdsLun::RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) method to delete the plex.</span></span> <span data-ttu-id="bcb2d-112">Vous pouvez interroger les plex LUN en appelant la méthode [**IVdsLun :: QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) .</span><span class="sxs-lookup"><span data-stu-id="bcb2d-112">You can query for LUN plexes by invoking the [**IVdsLun::QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) method.</span></span> <span data-ttu-id="bcb2d-113">Vous pouvez obtenir un pointeur vers un plex LUN spécifique en sélectionnant l’objet Plex souhaité à partir de l’énumération retournée par la méthode **QueryPlexes** .</span><span class="sxs-lookup"><span data-stu-id="bcb2d-113">You can get a pointer to a specific LUN plex by selecting the desired plex object from the enumeration that is returned by the **QueryPlexes** method.</span></span> <span data-ttu-id="bcb2d-114">Avec un objet Plex, vous pouvez rechercher les étendues de lecteur et les indicateurs automagic, et appliquer de nouveaux indicateurs.</span><span class="sxs-lookup"><span data-stu-id="bcb2d-114">With a plex object, you can query for the drive extents and automagic hints, and apply new hints.</span></span>

<span data-ttu-id="bcb2d-115">En plus de l’identificateur d’objet, d’un nom et d’un numéro de série, les propriétés des objets LUN Plex incluent le type, la taille, l’État, l’intégrité, l’état de transition et les indicateurs du Plex. une liste de démasquage et une taille d’entrelacement ; et un paramètre de priorité de reconstruction.</span><span class="sxs-lookup"><span data-stu-id="bcb2d-115">In addition to an object identifier, a name, and a serial number, LUN plex object properties include the plex type, size, status, health, transition state, and flags; an unmasking list and stripe size; and a rebuild priority setting.</span></span>

<span data-ttu-id="bcb2d-116">Le tableau suivant répertorie les interfaces, énumérations et structures associées.</span><span class="sxs-lookup"><span data-stu-id="bcb2d-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="bcb2d-117">Type</span><span class="sxs-lookup"><span data-stu-id="bcb2d-117">Type</span></span>                                              | <span data-ttu-id="bcb2d-118">Élément</span><span class="sxs-lookup"><span data-stu-id="bcb2d-118">Element</span></span>                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb2d-119">Interfaces toujours exposées par cet objet</span><span class="sxs-lookup"><span data-stu-id="bcb2d-119">Interfaces that are always exposed by this object</span></span> | <span data-ttu-id="bcb2d-120">[**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).</span><span class="sxs-lookup"><span data-stu-id="bcb2d-120">[**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).</span></span>                                                                                                                              |
| <span data-ttu-id="bcb2d-121">Énumérations associées</span><span class="sxs-lookup"><span data-stu-id="bcb2d-121">Associated enumerations</span></span>                           | <span data-ttu-id="bcb2d-122">[**VDS \_ \_ \_ Indicateur de plex LUN**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**\_ \_ \_ État du Plex LUN VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)et [**\_ \_ \_ type de plex LUN VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type).</span><span class="sxs-lookup"><span data-stu-id="bcb2d-122">[**VDS\_LUN\_PLEX\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**VDS\_LUN\_PLEX\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status), and [**VDS\_LUN\_PLEX\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type).</span></span> |
| <span data-ttu-id="bcb2d-123">Structures associées</span><span class="sxs-lookup"><span data-stu-id="bcb2d-123">Associated structures</span></span>                             | <span data-ttu-id="bcb2d-124">[**VDS \_ LUN \_ Plex \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).</span><span class="sxs-lookup"><span data-stu-id="bcb2d-124">[**VDS\_LUN\_PLEX\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).</span></span>                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="bcb2d-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bcb2d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcb2d-126">Objets de fournisseur de matériel</span><span class="sxs-lookup"><span data-stu-id="bcb2d-126">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="bcb2d-127">LUN (objet)</span><span class="sxs-lookup"><span data-stu-id="bcb2d-127">LUN Object</span></span>](lun-object.md)
</dt> </dl>

 

 
