---
title: IVMVirtualPC MaximumParallelPortsPerVM, propriété (VPCCOMInterfaces. h)
description: Récupère le nombre maximal de ports parallèles par ordinateur virtuel.
ms.assetid: c5baac59-386c-4373-a560-460750178894
keywords:
- MaximumParallelPortsPerVM propriété Virtual PC
- MaximumParallelPortsPerVM, propriété Virtual PC, IVMVirtualPC, interface
- IVMVirtualPC interface Virtual PC, propriété MaximumParallelPortsPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumParallelPortsPerVM
- IVMVirtualPC.get_MaximumParallelPortsPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c5bed446a421190eb47630bde0d05f0cbcee7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518081"
---
# <a name="ivmvirtualpcmaximumparallelportspervm-property"></a><span data-ttu-id="00102-106">IVMVirtualPC :: MaximumParallelPortsPerVM, propriété</span><span class="sxs-lookup"><span data-stu-id="00102-106">IVMVirtualPC::MaximumParallelPortsPerVM property</span></span>

<span data-ttu-id="00102-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="00102-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="00102-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="00102-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="00102-109">Récupère le nombre maximal de ports parallèles par ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="00102-109">Retrieves the maximum number of parallel ports per virtual machine.</span></span>

<span data-ttu-id="00102-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="00102-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="00102-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00102-111">Syntax</span></span>


```C++
HRESULT get_MaximumParallelPortsPerVM(
  [out, retval] long *maxPorts
);
```



## <a name="property-value"></a><span data-ttu-id="00102-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="00102-112">Property value</span></span>

<span data-ttu-id="00102-113">Nombre maximal de ports parallèles par ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="00102-113">The maximum number of parallel ports per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="00102-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="00102-114">Error codes</span></span>



| <span data-ttu-id="00102-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="00102-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="00102-116">Signification</span><span class="sxs-lookup"><span data-stu-id="00102-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="00102-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="00102-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="00102-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="00102-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="00102-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="00102-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="00102-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="00102-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="00102-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="00102-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="00102-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="00102-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="00102-123"><dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="00102-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="00102-124">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="00102-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="00102-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00102-125">Requirements</span></span>



| <span data-ttu-id="00102-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00102-126">Requirement</span></span> | <span data-ttu-id="00102-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="00102-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="00102-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00102-128">Minimum supported client</span></span><br/> | <span data-ttu-id="00102-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00102-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="00102-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00102-130">Minimum supported server</span></span><br/> | <span data-ttu-id="00102-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="00102-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="00102-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="00102-132">End of client support</span></span><br/>    | <span data-ttu-id="00102-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="00102-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="00102-134">Produit</span><span class="sxs-lookup"><span data-stu-id="00102-134">Product</span></span><br/>                  | <span data-ttu-id="00102-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="00102-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="00102-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="00102-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="00102-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="00102-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="00102-138">IID</span><span class="sxs-lookup"><span data-stu-id="00102-138">IID</span></span><br/>                      | <span data-ttu-id="00102-139">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="00102-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="00102-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00102-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00102-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="00102-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

