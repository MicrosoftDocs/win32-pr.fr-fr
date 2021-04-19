---
title: IVMVirtualPC VirtualMachines, propriété (VPCCOMInterfaces. h)
description: Récupère une collection énumérable de machines virtuelles.
ms.assetid: 9e8dcd65-7cf8-4cdd-a412-62cbb96eb8ec
keywords:
- VirtualMachines propriété Virtual PC
- VirtualMachines, propriété Virtual PC, IVMVirtualPC, interface
- IVMVirtualPC interface Virtual PC, propriété VirtualMachines
topic_type:
- apiref
api_name:
- IVMVirtualPC.VirtualMachines
- IVMVirtualPC.get_VirtualMachines
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44e141208994fa3d759074e7cbb294e1e2158917
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106514258"
---
# <a name="ivmvirtualpcvirtualmachines-property"></a><span data-ttu-id="a2cc1-106">IVMVirtualPC :: VirtualMachines, propriété</span><span class="sxs-lookup"><span data-stu-id="a2cc1-106">IVMVirtualPC::VirtualMachines property</span></span>

<span data-ttu-id="a2cc1-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a2cc1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a2cc1-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a2cc1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a2cc1-109">Récupère une collection énumérable de machines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="a2cc1-109">Retrieves an enumerable collection of virtual machines.</span></span>

<span data-ttu-id="a2cc1-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a2cc1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2cc1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2cc1-111">Syntax</span></span>


```C++
HRESULT get_VirtualMachines(
  [out, retval] IVMVirtualMachineCollection **virtualMachineCollection
);
```



## <a name="property-value"></a><span data-ttu-id="a2cc1-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a2cc1-112">Property value</span></span>

<span data-ttu-id="a2cc1-113">Collection d’objets [**IVMVirtualMachine**](ivmvirtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="a2cc1-113">A collection of [**IVMVirtualMachine**](ivmvirtualmachine.md) objects.</span></span> <span data-ttu-id="a2cc1-114">Consultez [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md).</span><span class="sxs-lookup"><span data-stu-id="a2cc1-114">See [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="a2cc1-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a2cc1-115">Error codes</span></span>



| <span data-ttu-id="a2cc1-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="a2cc1-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="a2cc1-117">Signification</span><span class="sxs-lookup"><span data-stu-id="a2cc1-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a2cc1-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a2cc1-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="a2cc1-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a2cc1-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a2cc1-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a2cc1-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="a2cc1-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a2cc1-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="a2cc1-122"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a2cc1-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="a2cc1-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a2cc1-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="a2cc1-124"><dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="a2cc1-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="a2cc1-125">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="a2cc1-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a2cc1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2cc1-126">Requirements</span></span>



| <span data-ttu-id="a2cc1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2cc1-127">Requirement</span></span> | <span data-ttu-id="a2cc1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2cc1-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2cc1-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2cc1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a2cc1-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2cc1-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2cc1-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2cc1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a2cc1-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2cc1-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a2cc1-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a2cc1-133">End of client support</span></span><br/>    | <span data-ttu-id="a2cc1-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a2cc1-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a2cc1-135">Produit</span><span class="sxs-lookup"><span data-stu-id="a2cc1-135">Product</span></span><br/>                  | <span data-ttu-id="a2cc1-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a2cc1-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a2cc1-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2cc1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2cc1-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2cc1-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a2cc1-139">IID</span><span class="sxs-lookup"><span data-stu-id="a2cc1-139">IID</span></span><br/>                      | <span data-ttu-id="a2cc1-140">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="a2cc1-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a2cc1-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2cc1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2cc1-142">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="a2cc1-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

