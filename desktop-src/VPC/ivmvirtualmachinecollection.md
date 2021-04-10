---
title: Interface IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Définit la collection de machines virtuelles au sein de Windows Virtual PC. Pour obtenir un objet IVMVirtualMachineCollection, utilisez la propriété VirtualMachines IVMVirtualPC.
ms.assetid: 3d34e791-2dba-4529-b489-96a0c6227294
keywords:
- Virtual PC de l’interface IVMVirtualMachineCollection
- IVMVirtualMachineCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27426f96e409a1e67eb519e7a864ee7461879a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105646"
---
# <a name="ivmvirtualmachinecollection-interface"></a><span data-ttu-id="b72df-106">Interface IVMVirtualMachineCollection</span><span class="sxs-lookup"><span data-stu-id="b72df-106">IVMVirtualMachineCollection interface</span></span>

<span data-ttu-id="b72df-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b72df-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b72df-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b72df-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b72df-109">Définit la collection de machines virtuelles au sein de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="b72df-109">Defines the collection of virtual machines within Windows Virtual PC.</span></span> <span data-ttu-id="b72df-110">Pour obtenir un objet **IVMVirtualMachineCollection** , utilisez la propriété [**IVMVirtualPC :: VirtualMachines**](ivmvirtualpc-virtualmachines.md) .</span><span class="sxs-lookup"><span data-stu-id="b72df-110">To obtain an **IVMVirtualMachineCollection** object, use the [**IVMVirtualPC::VirtualMachines**](ivmvirtualpc-virtualmachines.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="b72df-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b72df-111">Members</span></span>

<span data-ttu-id="b72df-112">L’interface **IVMVirtualMachineCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b72df-112">The **IVMVirtualMachineCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b72df-113">**IVMVirtualMachineCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b72df-113">**IVMVirtualMachineCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="b72df-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b72df-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b72df-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b72df-115">Properties</span></span>

<span data-ttu-id="b72df-116">L’interface **IVMVirtualMachineCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b72df-116">The **IVMVirtualMachineCollection** interface has these properties.</span></span>



| <span data-ttu-id="b72df-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="b72df-117">Property</span></span>                                                             | <span data-ttu-id="b72df-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b72df-118">Access type</span></span>          | <span data-ttu-id="b72df-119">Description</span><span class="sxs-lookup"><span data-stu-id="b72df-119">Description</span></span>                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="b72df-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="b72df-120">**\_NewEnum**</span></span>](ivmvirtualmachinecollection--newenum.md)<br/> | <span data-ttu-id="b72df-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b72df-121">Read-only</span></span><br/> | <span data-ttu-id="b72df-122">Énumérateur de la collection.</span><span class="sxs-lookup"><span data-stu-id="b72df-122">An enumerator for the collection.</span></span><br/>                                   |
| [<span data-ttu-id="b72df-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="b72df-123">**Count**</span></span>](ivmvirtualmachinecollection-count.md)<br/>        | <span data-ttu-id="b72df-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b72df-124">Read-only</span></span><br/> | <span data-ttu-id="b72df-125">Nombre de machines virtuelles dans ce regroupement.</span><span class="sxs-lookup"><span data-stu-id="b72df-125">The number of virtual machines in this collection.</span></span><br/>                  |
| [<span data-ttu-id="b72df-126">**Élément**</span><span class="sxs-lookup"><span data-stu-id="b72df-126">**Item**</span></span>](ivmvirtualmachinecollection-item.md)<br/>          | <span data-ttu-id="b72df-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b72df-127">Read-only</span></span><br/> | <span data-ttu-id="b72df-128">Objet ordinateur virtuel qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="b72df-128">The virtual machine object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b72df-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b72df-129">Requirements</span></span>



| <span data-ttu-id="b72df-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b72df-130">Requirement</span></span> | <span data-ttu-id="b72df-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b72df-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b72df-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b72df-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b72df-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b72df-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b72df-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b72df-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b72df-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b72df-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b72df-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b72df-136">End of client support</span></span><br/>    | <span data-ttu-id="b72df-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b72df-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="b72df-138">Produit</span><span class="sxs-lookup"><span data-stu-id="b72df-138">Product</span></span><br/>                  | <span data-ttu-id="b72df-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b72df-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="b72df-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="b72df-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b72df-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b72df-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="b72df-142">IID</span><span class="sxs-lookup"><span data-stu-id="b72df-142">IID</span></span><br/>                      | <span data-ttu-id="b72df-143">IID \_ IVMVirtualMachineCollection est défini en tant que 59f31786-2a3d-4FBF-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="b72df-143">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b72df-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b72df-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b72df-145">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="b72df-145">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="b72df-146">**IVMVirtualPC :: VirtualMachines**</span><span class="sxs-lookup"><span data-stu-id="b72df-146">**IVMVirtualPC::VirtualMachines**</span></span>](ivmvirtualpc-virtualmachines.md)
</dt> </dl>

 

