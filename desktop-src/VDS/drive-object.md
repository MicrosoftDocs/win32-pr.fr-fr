---
description: Objet Drive
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Objet Drive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df8501c79f9381dba80a1fe0276014dccdf7a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203015"
---
# <a name="drive-object"></a><span data-ttu-id="fe840-103">Objet Drive</span><span class="sxs-lookup"><span data-stu-id="fe840-103">Drive Object</span></span>

<span data-ttu-id="fe840-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fe840-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="fe840-105">Un objet lecteur modélise un lecteur de disque physique qui est contenu dans un sous-système.</span><span class="sxs-lookup"><span data-stu-id="fe840-105">A drive object models a physical disk drive that is contained within a subsystem.</span></span> <span data-ttu-id="fe840-106">Chaque lecteur se connecte à un bus, occupe un emplacement et contient un ensemble d’étendues de lecteurs.</span><span class="sxs-lookup"><span data-stu-id="fe840-106">Each drive connects to a bus, occupies a slot, and contains a set of drive extents.</span></span> <span data-ttu-id="fe840-107">Chaque lecteur peut fournir des étendues à n’importe quel nombre de numéros d’unités logiques.</span><span class="sxs-lookup"><span data-stu-id="fe840-107">Each drive can contribute extents to any number of LUNs.</span></span> <span data-ttu-id="fe840-108">Un lecteur peut également être désigné comme disque de rechange à chaud.</span><span class="sxs-lookup"><span data-stu-id="fe840-108">A drive can also be designated as a hot spare.</span></span>

<span data-ttu-id="fe840-109">Utilisez la méthode [**IVdsSubSystem :: QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) pour déterminer les lecteurs contenus dans un sous-système spécifique.</span><span class="sxs-lookup"><span data-stu-id="fe840-109">Use the [**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) method to determine the drives that are contained by a specific subsystem.</span></span> <span data-ttu-id="fe840-110">Les appelants peuvent obtenir un pointeur vers un lecteur spécifique en sélectionnant l’objet lecteur souhaité dans l’énumération retournée par la méthode **QueryDrives** , ou en appelant la méthode [**IVdsSubSystem :: GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) et en passant le bus et le numéro d’emplacement souhaités.</span><span class="sxs-lookup"><span data-stu-id="fe840-110">Callers can get a pointer to a specific drive by selecting the desired drive object from the enumeration that is returned by the **QueryDrives** method, or by invoking the [**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) method and passing in the desired bus and slot number.</span></span> <span data-ttu-id="fe840-111">Avec un objet lecteur, vous pouvez définir l’état du lecteur et la requête pour les propriétés du lecteur, les étendues de lecteur associées et le sous-système contenant le lecteur.</span><span class="sxs-lookup"><span data-stu-id="fe840-111">With a drive object, you can set the drive status and query for drive properties, associated drive extents, and the subsystem containing the drive.</span></span>

<span data-ttu-id="fe840-112">En plus de l’identificateur d’objet, d’un nom et d’un numéro de série, les propriétés de l’objet lecteur incluent l’état du lecteur, l’intégrité et les indicateurs ; taille en octets ; et un numéro de bus et d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="fe840-112">In addition to an object identifier, a name, and a serial number, drive object properties include the drive status, health, and flags; the size in bytes; and a bus and slot number.</span></span>

<span data-ttu-id="fe840-113">Le tableau suivant répertorie les interfaces, énumérations et structures associées.</span><span class="sxs-lookup"><span data-stu-id="fe840-113">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="fe840-114">Type</span><span class="sxs-lookup"><span data-stu-id="fe840-114">Type</span></span>                                              | <span data-ttu-id="fe840-115">Élément</span><span class="sxs-lookup"><span data-stu-id="fe840-115">Element</span></span>                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe840-116">Interfaces toujours exposées par cet objet</span><span class="sxs-lookup"><span data-stu-id="fe840-116">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="fe840-117">**IVdsDrive**</span><span class="sxs-lookup"><span data-stu-id="fe840-117">**IVdsDrive**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| <span data-ttu-id="fe840-118">Interfaces qui peuvent être exposées par cet objet</span><span class="sxs-lookup"><span data-stu-id="fe840-118">Interfaces that may be exposed by this object</span></span>     | [<span data-ttu-id="fe840-119">**IVdsMaintenance**</span><span class="sxs-lookup"><span data-stu-id="fe840-119">**IVdsMaintenance**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| <span data-ttu-id="fe840-120">Énumérations associées</span><span class="sxs-lookup"><span data-stu-id="fe840-120">Associated enumerations</span></span>                           | <span data-ttu-id="fe840-121">[**VDS \_ \_Indicateur de lecteur**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**\_ \_ État du lecteur VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)et [**\_ \_ étendue du lecteur VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent).</span><span class="sxs-lookup"><span data-stu-id="fe840-121">[**VDS\_DRIVE\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**VDS\_DRIVE\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status), and [**VDS\_DRIVE\_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent).</span></span> |
| <span data-ttu-id="fe840-122">Structures associées</span><span class="sxs-lookup"><span data-stu-id="fe840-122">Associated structures</span></span>                             | <span data-ttu-id="fe840-123">[**VDS \_ La \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) . du lecteur et la [**\_ \_ notification du lecteur VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).</span><span class="sxs-lookup"><span data-stu-id="fe840-123">[**VDS\_DRIVE\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) and [**VDS\_DRIVE\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).</span></span>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="fe840-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe840-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe840-125">Objets de fournisseur de matériel</span><span class="sxs-lookup"><span data-stu-id="fe840-125">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="fe840-126">**IVdsSubSystem::QueryDrives**</span><span class="sxs-lookup"><span data-stu-id="fe840-126">**IVdsSubSystem::QueryDrives**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[<span data-ttu-id="fe840-127">**IVdsSubSystem::GetDrive**</span><span class="sxs-lookup"><span data-stu-id="fe840-127">**IVdsSubSystem::GetDrive**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
