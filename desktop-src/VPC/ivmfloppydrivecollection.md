---
title: Interface IVMFloppyDriveCollection (VPCCOMInterfaces. h)
description: Définit une collection de lecteurs de disquettes dans l’ordinateur virtuel.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- Virtual PC de l’interface IVMFloppyDriveCollection
- IVMFloppyDriveCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 664937a08bf7576c35b94a162fb5b6f4a7400f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385239"
---
# <a name="ivmfloppydrivecollection-interface"></a><span data-ttu-id="0d518-105">Interface IVMFloppyDriveCollection</span><span class="sxs-lookup"><span data-stu-id="0d518-105">IVMFloppyDriveCollection interface</span></span>

<span data-ttu-id="0d518-106">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0d518-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0d518-107">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0d518-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0d518-108">Définit une collection de lecteurs de disquettes dans l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0d518-108">Defines a collection of floppy drives within the virtual machine.</span></span> <span data-ttu-id="0d518-109">Pour obtenir un objet **IVMFloppyDriveCollection** , utilisez la propriété [**IVMVirtualMachine :: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .</span><span class="sxs-lookup"><span data-stu-id="0d518-109">To obtain an **IVMFloppyDriveCollection** object, use the [**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="0d518-110">Membres</span><span class="sxs-lookup"><span data-stu-id="0d518-110">Members</span></span>

<span data-ttu-id="0d518-111">L’interface **IVMFloppyDriveCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="0d518-111">The **IVMFloppyDriveCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="0d518-112">**IVMFloppyDriveCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0d518-112">**IVMFloppyDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="0d518-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0d518-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d518-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0d518-114">Properties</span></span>

<span data-ttu-id="0d518-115">L’interface **IVMFloppyDriveCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0d518-115">The **IVMFloppyDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="0d518-116">Propriété</span><span class="sxs-lookup"><span data-stu-id="0d518-116">Property</span></span>                                                          | <span data-ttu-id="0d518-117">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="0d518-117">Access type</span></span>          | <span data-ttu-id="0d518-118">Description</span><span class="sxs-lookup"><span data-stu-id="0d518-118">Description</span></span>                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="0d518-119">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="0d518-119">**\_NewEnum**</span></span>](ivmfloppydrivecollection--newenum.md)<br/> | <span data-ttu-id="0d518-120">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d518-120">Read-only</span></span><br/> | <span data-ttu-id="0d518-121">Énumérateur de la collection.</span><span class="sxs-lookup"><span data-stu-id="0d518-121">An enumerator for the collection.</span></span><br/>                                |
| [<span data-ttu-id="0d518-122">**Saut**</span><span class="sxs-lookup"><span data-stu-id="0d518-122">**Count**</span></span>](ivmfloppydrivecollection-count.md)<br/>        | <span data-ttu-id="0d518-123">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d518-123">Read-only</span></span><br/> | <span data-ttu-id="0d518-124">Nombre de lecteurs de disquette dans ce regroupement.</span><span class="sxs-lookup"><span data-stu-id="0d518-124">The number of floppy drives in this collection.</span></span><br/>                  |
| [<span data-ttu-id="0d518-125">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0d518-125">**Item**</span></span>](ivmfloppydrivecollection-item.md)<br/>          | <span data-ttu-id="0d518-126">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0d518-126">Read-only</span></span><br/> | <span data-ttu-id="0d518-127">Objet lecteur de disquette qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="0d518-127">The floppy drive object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0d518-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d518-128">Requirements</span></span>



| <span data-ttu-id="0d518-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d518-129">Requirement</span></span> | <span data-ttu-id="0d518-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d518-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d518-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d518-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0d518-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d518-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d518-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d518-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0d518-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d518-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0d518-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0d518-135">End of client support</span></span><br/>    | <span data-ttu-id="0d518-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0d518-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0d518-137">Produit</span><span class="sxs-lookup"><span data-stu-id="0d518-137">Product</span></span><br/>                  | <span data-ttu-id="0d518-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0d518-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0d518-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d518-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d518-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d518-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0d518-141">IID</span><span class="sxs-lookup"><span data-stu-id="0d518-141">IID</span></span><br/>                      | <span data-ttu-id="0d518-142">IID \_ IVMFloppyDriveCollection est défini en tant que 8ba70a25-F698-4EE5-85ce-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="0d518-142">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="0d518-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d518-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d518-144">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="0d518-144">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> <dt>

[<span data-ttu-id="0d518-145">**IVMVirtualMachine::FloppyDrives**</span><span class="sxs-lookup"><span data-stu-id="0d518-145">**IVMVirtualMachine::FloppyDrives**</span></span>](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

