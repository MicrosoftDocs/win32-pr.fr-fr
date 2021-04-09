---
title: IVMVirtualPC MaximumSerialPortsPerVM, propriété (VPCCOMInterfaces. h)
description: Récupère le nombre maximal de ports série par ordinateur virtuel.
ms.assetid: e7b874df-105e-4ca8-90ec-2368071dafa0
keywords:
- MaximumSerialPortsPerVM propriété Virtual PC
- MaximumSerialPortsPerVM, propriété Virtual PC, IVMVirtualPC, interface
- IVMVirtualPC interface Virtual PC, propriété MaximumSerialPortsPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumSerialPortsPerVM
- IVMVirtualPC.get_MaximumSerialPortsPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63aa00c56add6bc48f4c33626a84a854b025c81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102789"
---
# <a name="ivmvirtualpcmaximumserialportspervm-property"></a><span data-ttu-id="0b3d6-106">IVMVirtualPC :: MaximumSerialPortsPerVM, propriété</span><span class="sxs-lookup"><span data-stu-id="0b3d6-106">IVMVirtualPC::MaximumSerialPortsPerVM property</span></span>

<span data-ttu-id="0b3d6-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0b3d6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0b3d6-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0b3d6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0b3d6-109">Récupère le nombre maximal de ports série par ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0b3d6-109">Retrieves the maximum number of serial ports per virtual machine.</span></span>

<span data-ttu-id="0b3d6-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0b3d6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b3d6-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b3d6-111">Syntax</span></span>


```C++
HRESULT get_MaximumSerialPortsPerVM(
  [out, retval] long *maxPorts
);
```



## <a name="property-value"></a><span data-ttu-id="0b3d6-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0b3d6-112">Property value</span></span>

<span data-ttu-id="0b3d6-113">Nombre maximal de ports série par ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="0b3d6-113">The maximum number of serial ports per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0b3d6-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0b3d6-114">Error codes</span></span>



| <span data-ttu-id="0b3d6-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="0b3d6-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="0b3d6-116">Signification</span><span class="sxs-lookup"><span data-stu-id="0b3d6-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0b3d6-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0b3d6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="0b3d6-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0b3d6-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="0b3d6-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0b3d6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="0b3d6-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0b3d6-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="0b3d6-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0b3d6-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="0b3d6-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0b3d6-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="0b3d6-123"><dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="0b3d6-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="0b3d6-124">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="0b3d6-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0b3d6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b3d6-125">Requirements</span></span>



| <span data-ttu-id="0b3d6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b3d6-126">Requirement</span></span> | <span data-ttu-id="0b3d6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b3d6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b3d6-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b3d6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0b3d6-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b3d6-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b3d6-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b3d6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0b3d6-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b3d6-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0b3d6-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0b3d6-132">End of client support</span></span><br/>    | <span data-ttu-id="0b3d6-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b3d6-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0b3d6-134">Produit</span><span class="sxs-lookup"><span data-stu-id="0b3d6-134">Product</span></span><br/>                  | <span data-ttu-id="0b3d6-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0b3d6-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0b3d6-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b3d6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b3d6-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b3d6-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0b3d6-138">IID</span><span class="sxs-lookup"><span data-stu-id="0b3d6-138">IID</span></span><br/>                      | <span data-ttu-id="0b3d6-139">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="0b3d6-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0b3d6-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b3d6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b3d6-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="0b3d6-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

