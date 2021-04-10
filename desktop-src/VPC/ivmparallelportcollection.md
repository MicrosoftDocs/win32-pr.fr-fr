---
title: Interface IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Définit la collection de ports parallèles dans l’ordinateur virtuel. Pour obtenir un objet IVMParallelPortCollection, utilisez la propriété ParallelPorts IVMVirtualMachine.
ms.assetid: 038a5c08-cd92-426f-a059-9a4c2110548d
keywords:
- Virtual PC de l’interface IVMParallelPortCollection
- IVMParallelPortCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMParallelPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8284b3720e0272147c932cfbfd70448babf5606f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106051"
---
# <a name="ivmparallelportcollection-interface"></a><span data-ttu-id="c3236-106">Interface IVMParallelPortCollection</span><span class="sxs-lookup"><span data-stu-id="c3236-106">IVMParallelPortCollection interface</span></span>

<span data-ttu-id="c3236-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c3236-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c3236-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c3236-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c3236-109">Définit la collection de ports parallèles dans l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="c3236-109">Defines the collection of parallel ports within the virtual machine.</span></span> <span data-ttu-id="c3236-110">Pour obtenir un objet **IVMParallelPortCollection** , utilisez la propriété [**IVMVirtualMachine ::P arallelports**](ivmvirtualmachine-parallelports.md) .</span><span class="sxs-lookup"><span data-stu-id="c3236-110">To obtain an **IVMParallelPortCollection** object, use the [**IVMVirtualMachine::ParallelPorts**](ivmvirtualmachine-parallelports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="c3236-111">Membres</span><span class="sxs-lookup"><span data-stu-id="c3236-111">Members</span></span>

<span data-ttu-id="c3236-112">L’interface **IVMParallelPortCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="c3236-112">The **IVMParallelPortCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c3236-113">**IVMParallelPortCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c3236-113">**IVMParallelPortCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="c3236-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c3236-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3236-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c3236-115">Properties</span></span>

<span data-ttu-id="c3236-116">L’interface **IVMParallelPortCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c3236-116">The **IVMParallelPortCollection** interface has these properties.</span></span>



| <span data-ttu-id="c3236-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="c3236-117">Property</span></span>                                                           | <span data-ttu-id="c3236-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="c3236-118">Access type</span></span>          | <span data-ttu-id="c3236-119">Description</span><span class="sxs-lookup"><span data-stu-id="c3236-119">Description</span></span>                                                                  |
|:-------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="c3236-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="c3236-120">**\_NewEnum**</span></span>](ivmparallelportcollection--newenum.md)<br/> | <span data-ttu-id="c3236-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3236-121">Read-only</span></span><br/> | <span data-ttu-id="c3236-122">Énumérateur de la collection.</span><span class="sxs-lookup"><span data-stu-id="c3236-122">An enumerator for the collection.</span></span><br/>                                 |
| [<span data-ttu-id="c3236-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="c3236-123">**Count**</span></span>](ivmparallelportcollection-count.md)<br/>        | <span data-ttu-id="c3236-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3236-124">Read-only</span></span><br/> | <span data-ttu-id="c3236-125">Nombre de ports parallèles dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="c3236-125">The number of parallel ports in this collection.</span></span><br/>                  |
| [<span data-ttu-id="c3236-126">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c3236-126">**Item**</span></span>](ivmparallelportcollection-item.md)<br/>          | <span data-ttu-id="c3236-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c3236-127">Read-only</span></span><br/> | <span data-ttu-id="c3236-128">Objet de port parallèle qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="c3236-128">The parallel port object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c3236-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3236-129">Requirements</span></span>



| <span data-ttu-id="c3236-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3236-130">Requirement</span></span> | <span data-ttu-id="c3236-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3236-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3236-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3236-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c3236-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3236-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3236-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3236-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c3236-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3236-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c3236-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c3236-136">End of client support</span></span><br/>    | <span data-ttu-id="c3236-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3236-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c3236-138">Produit</span><span class="sxs-lookup"><span data-stu-id="c3236-138">Product</span></span><br/>                  | <span data-ttu-id="c3236-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c3236-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c3236-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3236-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3236-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3236-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c3236-142">IID</span><span class="sxs-lookup"><span data-stu-id="c3236-142">IID</span></span><br/>                      | <span data-ttu-id="c3236-143">IID \_ IVMParallelPortCollection est défini en tant que 27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="c3236-143">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c3236-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3236-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3236-145">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="c3236-145">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> <dt>

[<span data-ttu-id="c3236-146">**IVMVirtualMachine ::P arallelPorts**</span><span class="sxs-lookup"><span data-stu-id="c3236-146">**IVMVirtualMachine::ParallelPorts**</span></span>](ivmvirtualmachine-parallelports.md)
</dt> </dl>

 

