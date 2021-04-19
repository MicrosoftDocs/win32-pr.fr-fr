---
description: Un objet de pool de stockage modélise un pool de stockage dans un sous-système de stockage.
ms.assetid: a6104742-3ef9-4570-9728-3e6580953117
title: Objet de pool de stockage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44719b825193faa75546ba1a0f7b42155a3e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534139"
---
# <a name="storage-pool-object"></a><span data-ttu-id="611ad-103">Objet de pool de stockage</span><span class="sxs-lookup"><span data-stu-id="611ad-103">Storage Pool Object</span></span>

<span data-ttu-id="611ad-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="611ad-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="611ad-105">Un objet de pool de stockage modélise un pool de stockage dans un sous-système de stockage.</span><span class="sxs-lookup"><span data-stu-id="611ad-105">A storage pool object models a storage pool in a storage subsystem.</span></span>

<span data-ttu-id="611ad-106">Un pool de stockage contient des extensions de lecteur d’un ou plusieurs lecteurs qui sont gérés par le même fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="611ad-106">A storage pool contains drive extents from one or more drives that are managed by the same hardware provider.</span></span>

<span data-ttu-id="611ad-107">Le tableau suivant répertorie les interfaces, énumérations et structures associées.</span><span class="sxs-lookup"><span data-stu-id="611ad-107">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="611ad-108">Type</span><span class="sxs-lookup"><span data-stu-id="611ad-108">Type</span></span>                                              | <span data-ttu-id="611ad-109">Élément</span><span class="sxs-lookup"><span data-stu-id="611ad-109">Element</span></span>                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="611ad-110">Interfaces toujours exposées par cet objet</span><span class="sxs-lookup"><span data-stu-id="611ad-110">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="611ad-111">**IVdsStoragePool**</span><span class="sxs-lookup"><span data-stu-id="611ad-111">**IVdsStoragePool**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| <span data-ttu-id="611ad-112">Énumérations associées</span><span class="sxs-lookup"><span data-stu-id="611ad-112">Associated enumerations</span></span>                           | <span data-ttu-id="611ad-113">[**VDS \_ \_Type RAID**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**\_ État du \_ pool \_ de stockage VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)et [**type de \_ \_ pool \_ de stockage VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).</span><span class="sxs-lookup"><span data-stu-id="611ad-113">[**VDS\_RAID\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**VDS\_STORAGE\_POOL\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status), and [**VDS\_STORAGE\_POOL\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).</span></span>                                                                                                                                  |
| <span data-ttu-id="611ad-114">Structures associées</span><span class="sxs-lookup"><span data-stu-id="611ad-114">Associated structures</span></span>                             | <span data-ttu-id="611ad-115">[**VDS \_ HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**\_ \_ attributs de pool VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**\_ \_ \_ attributs personnalisés du pool VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**\_ \_ \_ \_ étendue du lecteur du pool de stockage VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)et pool de [**stockage VDS \_ \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop).</span><span class="sxs-lookup"><span data-stu-id="611ad-115">[**VDS\_HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**VDS\_POOL\_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**VDS\_POOL\_CUSTOM\_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**VDS\_STORAGE\_POOL\_DRIVE\_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent), and [**VDS\_STORAGE\_POOL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop).</span></span> |



 

 

 
