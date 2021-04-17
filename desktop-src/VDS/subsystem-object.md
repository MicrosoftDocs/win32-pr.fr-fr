---
description: SUBSYSTEM (objet)
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: SUBSYSTEM (objet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8314a798ea809b3175377bc5484f19629094db
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104567753"
---
# <a name="subsystem-object"></a><span data-ttu-id="b5b84-103">SUBSYSTEM (objet)</span><span class="sxs-lookup"><span data-stu-id="b5b84-103">Subsystem Object</span></span>

<span data-ttu-id="b5b84-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b5b84-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="b5b84-105">Un objet sous-système modélise un sous-système de stockage.</span><span class="sxs-lookup"><span data-stu-id="b5b84-105">A subsystem object models a storage subsystem.</span></span> <span data-ttu-id="b5b84-106">Un sous-système est soit un boîtier RAID, soit une carte RAID PCI.</span><span class="sxs-lookup"><span data-stu-id="b5b84-106">A subsystem is either a RAID enclosure or a PCI RAID card.</span></span> <span data-ttu-id="b5b84-107">Un seul ordinateur hôte peut être connecté à n’importe quel nombre de sous-systèmes.</span><span class="sxs-lookup"><span data-stu-id="b5b84-107">A single host computer can be connected to any number of subsystems.</span></span> <span data-ttu-id="b5b84-108">Chaque sous-système est géré par un seul fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="b5b84-108">Each subsystem is managed by exactly one hardware provider.</span></span> <span data-ttu-id="b5b84-109">Dans une configuration SAN, la classe de sous-système représente un boîtier de stockage SAN.</span><span class="sxs-lookup"><span data-stu-id="b5b84-109">In a SAN configuration, the subsystem class represents a SAN storage enclosure.</span></span>

<span data-ttu-id="b5b84-110">Un sous-système peut contenir un nombre quelconque de contrôleurs et de lecteurs, et peut surfacer (démasquer) un nombre quelconque de numéros d’unités logiques sur l’ordinateur sur lequel le fournisseur de matériel s’exécute.</span><span class="sxs-lookup"><span data-stu-id="b5b84-110">A subsystem can contain any number of controllers and drives, and can surface (unmask) any number of LUNs to the computer on which the hardware provider is running.</span></span> <span data-ttu-id="b5b84-111">Les sous-systèmes de plus haut niveau peuvent démasquer des numéros d’unités logiques sur d’autres ordinateurs sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="b5b84-111">Higher-end subsystems can unmask LUNs to other computers on the network.</span></span> <span data-ttu-id="b5b84-112">Chaque lecteur de disque d’un sous-système est connecté à un bus et occupe un emplacement dans le bus.</span><span class="sxs-lookup"><span data-stu-id="b5b84-112">Each disk drive within a subsystem is connected to a bus and occupies a slot in the bus.</span></span> <span data-ttu-id="b5b84-113">Chaque contrôleur au sein d’un sous-système possède un ou plusieurs ports de contrôleur.</span><span class="sxs-lookup"><span data-stu-id="b5b84-113">Each controller within a subsystem has one or more controller ports.</span></span>

<span data-ttu-id="b5b84-114">L’illustration suivante montre les périphériques physiques contenus dans un sous-système (les numéros d’unités logiques ne sont pas affichés) et les relations entre eux.</span><span class="sxs-lookup"><span data-stu-id="b5b84-114">The illustration that follows shows the physical devices contained in a subsystem (LUNs are not shown) and the relationships among them.</span></span>

![Diagramme montrant un sous-système commençant par « ports » sur la gauche, passant à « Controllers », puis un « bus » avec « Slots » menant à des « lecteurs » individuels.](images/vdssubsystem.png)

<span data-ttu-id="b5b84-116">Les applications VDS utilisent la méthode [**IVdsHwProvider :: QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) pour interroger les sous-systèmes appartenant à un fournisseur de matériel spécifique.</span><span class="sxs-lookup"><span data-stu-id="b5b84-116">VDS applications use the [**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) method to query the subsystems that belong to a specific hardware provider.</span></span> <span data-ttu-id="b5b84-117">Les appelants peuvent obtenir un pointeur vers un sous-système spécifique en sélectionnant l’objet sous-système souhaité à partir de l’énumération retournée par la méthode **QuerySubSystems** .</span><span class="sxs-lookup"><span data-stu-id="b5b84-117">Callers can get a pointer to a specific subsystem by selecting the desired subsystem object from the enumeration that is returned by the **QuerySubSystems** method.</span></span> <span data-ttu-id="b5b84-118">Avec un objet de sous-système, vous pouvez définir l’état du sous-système, créer des numéros d’unités logiques, remplacer les lecteurs et interroger les contrôleurs, les lecteurs et les numéros d’unités logiques.</span><span class="sxs-lookup"><span data-stu-id="b5b84-118">With a subsystem object, you can set the subsystem status, create LUNs, replace drives, and query for controllers, drives, and LUNs.</span></span>

<span data-ttu-id="b5b84-119">En plus de l’identificateur d’objet, d’un nom et d’un numéro de série, les propriétés de l’objet sous-système incluent l’État, l’intégrité et les indicateurs du sous-système. le nombre de contrôleurs, d’emplacements et de bus ; et un paramètre de priorité de reconstruction.</span><span class="sxs-lookup"><span data-stu-id="b5b84-119">In addition to an object identifier, a name, and a serial number, subsystem object properties include the subsystem status, health, and flags; a count of the controllers, slots, and buses; and a rebuild priority setting.</span></span>

<span data-ttu-id="b5b84-120">Le tableau suivant répertorie les interfaces, énumérations et structures associées.</span><span class="sxs-lookup"><span data-stu-id="b5b84-120">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="b5b84-121">Type</span><span class="sxs-lookup"><span data-stu-id="b5b84-121">Type</span></span>                                                                                      | <span data-ttu-id="b5b84-122">Élément</span><span class="sxs-lookup"><span data-stu-id="b5b84-122">Element</span></span>                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5b84-123">Interfaces toujours exposées par cet objet</span><span class="sxs-lookup"><span data-stu-id="b5b84-123">Interfaces that are always exposed by this object</span></span>                                         | <span data-ttu-id="b5b84-124">[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).</span><span class="sxs-lookup"><span data-stu-id="b5b84-124">[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem).</span></span>                                                                                          |
| <span data-ttu-id="b5b84-125">Interfaces toujours exposées par cet objet dans les fournisseurs iSCSI VDS 1,1 et 2,0 uniquement</span><span class="sxs-lookup"><span data-stu-id="b5b84-125">Interfaces that are always exposed by this object in VDS 1.1 and 2.0 iSCSI providers only</span></span> | <span data-ttu-id="b5b84-126">[**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) et [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).</span><span class="sxs-lookup"><span data-stu-id="b5b84-126">[**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) and [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget).</span></span>             |
| <span data-ttu-id="b5b84-127">Interfaces qui peuvent être exposées par cet objet</span><span class="sxs-lookup"><span data-stu-id="b5b84-127">Interfaces that may be exposed by this object</span></span>                                             | <span data-ttu-id="b5b84-128">[**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) et [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).</span><span class="sxs-lookup"><span data-stu-id="b5b84-128">[**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) and [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance).</span></span>                               |
| <span data-ttu-id="b5b84-129">Énumérations associées</span><span class="sxs-lookup"><span data-stu-id="b5b84-129">Associated enumerations</span></span>                                                                   | <span data-ttu-id="b5b84-130">[**VDS \_ \_ \_ Indicateur de sous-système**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) et [**\_ État du sous \_ -système \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).</span><span class="sxs-lookup"><span data-stu-id="b5b84-130">[**VDS\_SUB\_SYSTEM\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) and [**VDS\_SUB\_SYSTEM\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status).</span></span>             |
| <span data-ttu-id="b5b84-131">Structures associées</span><span class="sxs-lookup"><span data-stu-id="b5b84-131">Associated structures</span></span>                                                                     | <span data-ttu-id="b5b84-132">[**VDS \_ SOUS \_ -système \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) et [**\_ notification du sous \_ -système \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification).</span><span class="sxs-lookup"><span data-stu-id="b5b84-132">[**VDS\_SUB\_SYSTEM\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) and [**VDS\_SUB\_SYSTEM\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b5b84-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5b84-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5b84-134">Objets de fournisseur de matériel</span><span class="sxs-lookup"><span data-stu-id="b5b84-134">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="b5b84-135">**IVdsHwProvider::QuerySubSystems**</span><span class="sxs-lookup"><span data-stu-id="b5b84-135">**IVdsHwProvider::QuerySubSystems**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
