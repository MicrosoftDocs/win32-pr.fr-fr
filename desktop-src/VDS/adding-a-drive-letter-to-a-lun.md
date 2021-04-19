---
description: Ajout d’une lettre de lecteur à un numéro d’unité logique
ms.assetid: 3f350312-3f1f-4020-90d0-85521ea9c7c8
title: Ajout d’une lettre de lecteur à un numéro d’unité logique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426a4f3bf720b21a02462edde4a381012d2084d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514167"
---
# <a name="adding-a-drive-letter-to-a-lun"></a><span data-ttu-id="bc8cb-103">Ajout d’une lettre de lecteur à un numéro d’unité logique</span><span class="sxs-lookup"><span data-stu-id="bc8cb-103">Adding a Drive Letter to a LUN</span></span>

<span data-ttu-id="bc8cb-104">\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bc8cb-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="bc8cb-105">Vous pouvez affecter des lettres de lecteur à des objets de volume directement ; Toutefois, si votre disque est un objet LUN, quelques étapes supplémentaires sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="bc8cb-105">You can assign drive letters to volume objects directly; however, if your disk is a LUN object, you have a few additional steps.</span></span>

<span data-ttu-id="bc8cb-106">**Pour affecter une lettre de lecteur à un objet LUN**</span><span class="sxs-lookup"><span data-stu-id="bc8cb-106">**To assign a drive letter to a LUN object**</span></span>

1.  <span data-ttu-id="bc8cb-107">Si nécessaire, démasquez le numéro d’unité logique à l’hôte local.</span><span class="sxs-lookup"><span data-stu-id="bc8cb-107">If necessary, unmask the LUN to the local host.</span></span>
    > [!Note]  
    > <span data-ttu-id="bc8cb-108">Vous ne pouvez pas effectuer d’opérations d’administration logicielle sur un objet LUN qui n’est pas masqué sur un autre ordinateur au sein de la session VDS en cours.</span><span class="sxs-lookup"><span data-stu-id="bc8cb-108">You cannot perform software administrative operations on a LUN object that is unmasked to another computer within the current VDS session.</span></span>

     

2.  <span data-ttu-id="bc8cb-109">Appelez la méthode [**IVdsService :: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) sur l’ordinateur qui exécute le fournisseur de matériel.</span><span class="sxs-lookup"><span data-stu-id="bc8cb-109">Invoke the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method on the computer that is running the hardware provider.</span></span>
3.  <span data-ttu-id="bc8cb-110">Initialisez le numéro d’unité logique en tant que disque de base, comme suit :</span><span class="sxs-lookup"><span data-stu-id="bc8cb-110">Initialize the LUN as a basic disk as follows:</span></span>
    1.  <span data-ttu-id="bc8cb-111">Appelez la méthode [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’objet lun pour interroger l’interface [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) .</span><span class="sxs-lookup"><span data-stu-id="bc8cb-111">Invoke the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the LUN object to query for the [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) interface.</span></span>
    2.  <span data-ttu-id="bc8cb-112">Appelez la méthode [**IVdsSwProvider :: CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) pour créer un pack de base.</span><span class="sxs-lookup"><span data-stu-id="bc8cb-112">Invoke the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a basic pack.</span></span>
    3.  <span data-ttu-id="bc8cb-113">Appelez la méthode [**IVdsPack :: AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) pour ajouter le disque au nouveau Pack.</span><span class="sxs-lookup"><span data-stu-id="bc8cb-113">Invoke the [**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) method to add the disk to the new pack.</span></span>
4.  <span data-ttu-id="bc8cb-114">Créez une partition sur le disque et obtenez l’objet volume comme suit :</span><span class="sxs-lookup"><span data-stu-id="bc8cb-114">Create a partition on the disk and obtain the volume object as follows:</span></span>
    1.  <span data-ttu-id="bc8cb-115">Appelez la méthode [**IVdsCreatePartitionEx :: CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) pour créer une partition.</span><span class="sxs-lookup"><span data-stu-id="bc8cb-115">Invoke the [**IVdsCreatePartitionEx::CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) method to create a partition.</span></span>
    2.  <span data-ttu-id="bc8cb-116">Appelez la méthode [**IVdsAsync :: wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) sur l’objet Async retourné par [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) pour récupérer l’identificateur de volume à partir de la structure de [**\_ \_ sortie asynchrone VDS**](/windows/desktop/api/Vds/ns-vds-vds_async_output) .</span><span class="sxs-lookup"><span data-stu-id="bc8cb-116">Invoke the [**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) method on the async object that is returned by [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) to get the volume identifier from the [**VDS\_ASYNC\_OUTPUT**](/windows/desktop/api/Vds/ns-vds-vds_async_output) structure.</span></span>
    3.  <span data-ttu-id="bc8cb-117">Transmettez l’identificateur de volume en tant que paramètre à la méthode [**IVdsService :: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) pour obtenir un pointeur d’objet de volume.</span><span class="sxs-lookup"><span data-stu-id="bc8cb-117">Pass the volume identifier as a parameter to the [**IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) method to get a volume object pointer.</span></span>
5.  <span data-ttu-id="bc8cb-118">Appelez la méthode [**IVdsVolumeMF :: AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) pour affecter la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="bc8cb-118">Invoke the [**IVdsVolumeMF::AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) method to assign the drive letter.</span></span>

> [!Note]  
> <span data-ttu-id="bc8cb-119">La méthode [**IVdsAdvancedDisk :: AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) affecte des lettres de lecteur à des partitions sans volumes associés, comme des partitions OEM ou ESP.</span><span class="sxs-lookup"><span data-stu-id="bc8cb-119">The [**IVdsAdvancedDisk::AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) method assigns drive letters to partitions without associated volumes, such as OEM or ESP partitions.</span></span> <span data-ttu-id="bc8cb-120">Vous ne pouvez pas l’utiliser pour affecter une lettre de lecteur à un objet LUN.</span><span class="sxs-lookup"><span data-stu-id="bc8cb-120">You cannot use it to assign a drive letter to a LUN object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bc8cb-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc8cb-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc8cb-122">Utilisation de VDS</span><span class="sxs-lookup"><span data-stu-id="bc8cb-122">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="bc8cb-123">**IVdsService :: réénumération**</span><span class="sxs-lookup"><span data-stu-id="bc8cb-123">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="bc8cb-124">**IVdsDisk**</span><span class="sxs-lookup"><span data-stu-id="bc8cb-124">**IVdsDisk**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[<span data-ttu-id="bc8cb-125">**IVdsSwProvider::CreatePack**</span><span class="sxs-lookup"><span data-stu-id="bc8cb-125">**IVdsSwProvider::CreatePack**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[<span data-ttu-id="bc8cb-126">**IVdsPack::AddDisk**</span><span class="sxs-lookup"><span data-stu-id="bc8cb-126">**IVdsPack::AddDisk**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[<span data-ttu-id="bc8cb-127">**IVdsCreatePartitionEx::CreatePartitionEx**</span><span class="sxs-lookup"><span data-stu-id="bc8cb-127">**IVdsCreatePartitionEx::CreatePartitionEx**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[<span data-ttu-id="bc8cb-128">**IVdsAsync :: wait**</span><span class="sxs-lookup"><span data-stu-id="bc8cb-128">**IVdsAsync::Wait**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[<span data-ttu-id="bc8cb-129">**\_sortie asynchrone \_ VDS**</span><span class="sxs-lookup"><span data-stu-id="bc8cb-129">**VDS\_ASYNC\_OUTPUT**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[<span data-ttu-id="bc8cb-130">**IVdsVolumeMF::AddAccessPath**</span><span class="sxs-lookup"><span data-stu-id="bc8cb-130">**IVdsVolumeMF::AddAccessPath**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[<span data-ttu-id="bc8cb-131">**IVdsAdvancedDisk::AssignDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="bc8cb-131">**IVdsAdvancedDisk::AssignDriveLetter**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
