---
title: Interface IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Définit la collection de lecteurs de CD et de DVD dans l’ordinateur virtuel. Pour obtenir un objet IVMDVDDriveCollection, utilisez la propriété DVDROMDrives IVMVirtualMachine.
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- Virtual PC de l’interface IVMDVDDriveCollection
- IVMDVDDriveCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6afcf14a1ffe53dea0dcd7e21fcde8729e0bd0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510757"
---
# <a name="ivmdvddrivecollection-interface"></a><span data-ttu-id="8e3f8-106">Interface IVMDVDDriveCollection</span><span class="sxs-lookup"><span data-stu-id="8e3f8-106">IVMDVDDriveCollection interface</span></span>

<span data-ttu-id="8e3f8-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8e3f8-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8e3f8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8e3f8-109">Définit la collection de lecteurs de CD et de DVD dans l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-109">Defines the collection of CD and DVD drives within the virtual machine.</span></span> <span data-ttu-id="8e3f8-110">Pour obtenir un objet **IVMDVDDriveCollection** , utilisez la propriété [**IVMVirtualMachine ::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .</span><span class="sxs-lookup"><span data-stu-id="8e3f8-110">To obtain an **IVMDVDDriveCollection** object, use the [**IVMVirtualMachine::DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="8e3f8-111">Membres</span><span class="sxs-lookup"><span data-stu-id="8e3f8-111">Members</span></span>

<span data-ttu-id="8e3f8-112">L’interface **IVMDVDDriveCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="8e3f8-112">The **IVMDVDDriveCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8e3f8-113">**IVMDVDDriveCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e3f8-113">**IVMDVDDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="8e3f8-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8e3f8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e3f8-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8e3f8-115">Properties</span></span>

<span data-ttu-id="8e3f8-116">L’interface **IVMDVDDriveCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-116">The **IVMDVDDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="8e3f8-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="8e3f8-117">Property</span></span>                                                       | <span data-ttu-id="8e3f8-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="8e3f8-118">Access type</span></span>          | <span data-ttu-id="8e3f8-119">Description</span><span class="sxs-lookup"><span data-stu-id="8e3f8-119">Description</span></span>                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="8e3f8-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="8e3f8-120">**\_NewEnum**</span></span>](ivmdvddrivecollection--newenum.md)<br/> | <span data-ttu-id="8e3f8-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8e3f8-121">Read-only</span></span><br/> | <span data-ttu-id="8e3f8-122">Énumérateur de la collection.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-122">An enumerator for the collection.</span></span><br/>                                   |
| [<span data-ttu-id="8e3f8-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="8e3f8-123">**Count**</span></span>](ivmdvddrivecollection-count.md)<br/>        | <span data-ttu-id="8e3f8-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8e3f8-124">Read-only</span></span><br/> | <span data-ttu-id="8e3f8-125">Nombre de lecteurs de CD et de DVD dans ce regroupement.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-125">The number of CD and DVD drives in this collection.</span></span><br/>                 |
| [<span data-ttu-id="8e3f8-126">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8e3f8-126">**Item**</span></span>](ivmdvddrivecollection-item.md)<br/>          | <span data-ttu-id="8e3f8-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8e3f8-127">Read-only</span></span><br/> | <span data-ttu-id="8e3f8-128">Objet lecteur de CD ou de DVD qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="8e3f8-128">The CD or DVD drive object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8e3f8-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e3f8-129">Requirements</span></span>



| <span data-ttu-id="8e3f8-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e3f8-130">Requirement</span></span> | <span data-ttu-id="8e3f8-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e3f8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e3f8-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e3f8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8e3f8-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e3f8-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8e3f8-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e3f8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8e3f8-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e3f8-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8e3f8-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8e3f8-136">End of client support</span></span><br/>    | <span data-ttu-id="8e3f8-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8e3f8-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8e3f8-138">Produit</span><span class="sxs-lookup"><span data-stu-id="8e3f8-138">Product</span></span><br/>                  | <span data-ttu-id="8e3f8-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8e3f8-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8e3f8-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e3f8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e3f8-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e3f8-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8e3f8-142">IID</span><span class="sxs-lookup"><span data-stu-id="8e3f8-142">IID</span></span><br/>                      | <span data-ttu-id="8e3f8-143">IID \_ IVMDVDDriveCollection est défini en tant que bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="8e3f8-143">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="8e3f8-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e3f8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e3f8-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="8e3f8-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> <dt>

[<span data-ttu-id="8e3f8-146">**IVMVirtualMachine ::D VDROMDrives**</span><span class="sxs-lookup"><span data-stu-id="8e3f8-146">**IVMVirtualMachine::DVDROMDrives**</span></span>](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 

