---
title: IVMVirtualMachine ConfigID, propriété (VPCCOMInterfaces. h)
description: Récupère l’identificateur unique de la machine virtuelle.
ms.assetid: e1679822-d733-4c7a-a5ad-82cbc24a6329
keywords:
- ConfigID propriété Virtual PC
- ConfigID, propriété Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété ConfigID
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ConfigID
- IVMVirtualMachine.get_ConfigID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 291a1faf3012016d35130b21ff4743faae25b794
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033067"
---
# <a name="ivmvirtualmachineconfigid-property"></a><span data-ttu-id="66fae-106">IVMVirtualMachine :: ConfigID, propriété</span><span class="sxs-lookup"><span data-stu-id="66fae-106">IVMVirtualMachine::ConfigID property</span></span>

<span data-ttu-id="66fae-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="66fae-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="66fae-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="66fae-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="66fae-109">Récupère l’identificateur unique de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="66fae-109">Retrieves the unique identifier for the virtual machine.</span></span>

<span data-ttu-id="66fae-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="66fae-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="66fae-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66fae-111">Syntax</span></span>


```C++
HRESULT get_ConfigID(
  [out, retval] BSTR *virtualMachineConfigID
);
```



## <a name="property-value"></a><span data-ttu-id="66fae-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="66fae-112">Property value</span></span>

<span data-ttu-id="66fae-113">ID unique qui identifie la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="66fae-113">The unique ID that identifies the virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="66fae-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="66fae-114">Error codes</span></span>



| <span data-ttu-id="66fae-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="66fae-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="66fae-116">Signification</span><span class="sxs-lookup"><span data-stu-id="66fae-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="66fae-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="66fae-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="66fae-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="66fae-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="66fae-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="66fae-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="66fae-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="66fae-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="66fae-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="66fae-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="66fae-122">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="66fae-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="66fae-123"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="66fae-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="66fae-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="66fae-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="66fae-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66fae-125">Requirements</span></span>



| <span data-ttu-id="66fae-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66fae-126">Requirement</span></span> | <span data-ttu-id="66fae-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="66fae-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="66fae-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66fae-128">Minimum supported client</span></span><br/> | <span data-ttu-id="66fae-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66fae-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66fae-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66fae-130">Minimum supported server</span></span><br/> | <span data-ttu-id="66fae-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="66fae-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="66fae-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="66fae-132">End of client support</span></span><br/>    | <span data-ttu-id="66fae-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="66fae-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="66fae-134">Produit</span><span class="sxs-lookup"><span data-stu-id="66fae-134">Product</span></span><br/>                  | <span data-ttu-id="66fae-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="66fae-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="66fae-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="66fae-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="66fae-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="66fae-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="66fae-138">IID</span><span class="sxs-lookup"><span data-stu-id="66fae-138">IID</span></span><br/>                      | <span data-ttu-id="66fae-139">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="66fae-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="66fae-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66fae-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66fae-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="66fae-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

