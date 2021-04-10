---
title: IVMVirtualPC MaximumMemoryPerVM, propriété (VPCCOMInterfaces. h)
description: Récupère la quantité maximale autorisée de mémoire physique par ordinateur virtuel, en mégaoctets.
ms.assetid: eb30dd6c-8f37-4cf9-9ed7-47925b5b1112
keywords:
- MaximumMemoryPerVM propriété Virtual PC
- MaximumMemoryPerVM, propriété Virtual PC, IVMVirtualPC, interface
- IVMVirtualPC interface Virtual PC, propriété MaximumMemoryPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumMemoryPerVM
- IVMVirtualPC.get_MaximumMemoryPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936d88c29df4be934e03d1c0b7bde60139bde268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843033"
---
# <a name="ivmvirtualpcmaximummemorypervm-property"></a><span data-ttu-id="57adb-106">IVMVirtualPC :: MaximumMemoryPerVM, propriété</span><span class="sxs-lookup"><span data-stu-id="57adb-106">IVMVirtualPC::MaximumMemoryPerVM property</span></span>

<span data-ttu-id="57adb-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="57adb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="57adb-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="57adb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="57adb-109">Récupère la quantité maximale autorisée de mémoire physique par ordinateur virtuel, en mégaoctets.</span><span class="sxs-lookup"><span data-stu-id="57adb-109">Retrieves the maximum allowable quantity of physical memory per virtual machine, in megabytes.</span></span>

<span data-ttu-id="57adb-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="57adb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="57adb-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57adb-111">Syntax</span></span>


```C++
HRESULT get_MaximumMemoryPerVM(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="57adb-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="57adb-112">Property value</span></span>

<span data-ttu-id="57adb-113">Quantité maximale autorisée, en mégaoctets, de la mémoire physique par ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="57adb-113">The maximum allowable quantity, in megabytes, of physical memory per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="57adb-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="57adb-114">Error codes</span></span>



| <span data-ttu-id="57adb-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="57adb-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="57adb-116">Signification</span><span class="sxs-lookup"><span data-stu-id="57adb-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="57adb-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="57adb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="57adb-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="57adb-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="57adb-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="57adb-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="57adb-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="57adb-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="57adb-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="57adb-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="57adb-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="57adb-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="57adb-123"><dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="57adb-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="57adb-124">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="57adb-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="57adb-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57adb-125">Requirements</span></span>



| <span data-ttu-id="57adb-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57adb-126">Requirement</span></span> | <span data-ttu-id="57adb-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="57adb-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="57adb-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57adb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="57adb-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57adb-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="57adb-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57adb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="57adb-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="57adb-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="57adb-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="57adb-132">End of client support</span></span><br/>    | <span data-ttu-id="57adb-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="57adb-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="57adb-134">Produit</span><span class="sxs-lookup"><span data-stu-id="57adb-134">Product</span></span><br/>                  | <span data-ttu-id="57adb-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="57adb-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="57adb-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="57adb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="57adb-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="57adb-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="57adb-138">IID</span><span class="sxs-lookup"><span data-stu-id="57adb-138">IID</span></span><br/>                      | <span data-ttu-id="57adb-139">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="57adb-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="57adb-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57adb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57adb-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="57adb-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

