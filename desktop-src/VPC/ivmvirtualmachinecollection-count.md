---
title: Propriété Count IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Récupère le nombre de machines virtuelles de cette collection.
ms.assetid: c1f38528-fd9b-4b86-aac6-de944379b92e
keywords:
- Propriété Count Virtual PC
- Propriété Count Virtual PC, IVMVirtualMachineCollection, interface
- IVMVirtualMachineCollection interface Virtual PC, propriété Count
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Count
- IVMVirtualMachineCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f641fad504c6dd593737cf35014813f49609a4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105649"
---
# <a name="ivmvirtualmachinecollectioncount-property"></a><span data-ttu-id="25b8f-106">IVMVirtualMachineCollection :: Count, propriété</span><span class="sxs-lookup"><span data-stu-id="25b8f-106">IVMVirtualMachineCollection::Count property</span></span>

<span data-ttu-id="25b8f-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="25b8f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="25b8f-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="25b8f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="25b8f-109">Récupère le nombre de machines virtuelles de cette collection.</span><span class="sxs-lookup"><span data-stu-id="25b8f-109">Retrieves the number of virtual machines in this collection.</span></span>

<span data-ttu-id="25b8f-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="25b8f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="25b8f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25b8f-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="25b8f-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="25b8f-112">Property value</span></span>

<span data-ttu-id="25b8f-113">Nombre d’ordinateurs virtuels.</span><span class="sxs-lookup"><span data-stu-id="25b8f-113">The number of virtual machines.</span></span>

## <a name="error-codes"></a><span data-ttu-id="25b8f-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="25b8f-114">Error codes</span></span>



| <span data-ttu-id="25b8f-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="25b8f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="25b8f-116">Signification</span><span class="sxs-lookup"><span data-stu-id="25b8f-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="25b8f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="25b8f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="25b8f-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="25b8f-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="25b8f-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="25b8f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="25b8f-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="25b8f-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="25b8f-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="25b8f-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="25b8f-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="25b8f-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="25b8f-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25b8f-123">Requirements</span></span>



| <span data-ttu-id="25b8f-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25b8f-124">Requirement</span></span> | <span data-ttu-id="25b8f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="25b8f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25b8f-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25b8f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="25b8f-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25b8f-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="25b8f-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25b8f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="25b8f-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="25b8f-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="25b8f-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="25b8f-130">End of client support</span></span><br/>    | <span data-ttu-id="25b8f-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="25b8f-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="25b8f-132">Produit</span><span class="sxs-lookup"><span data-stu-id="25b8f-132">Product</span></span><br/>                  | <span data-ttu-id="25b8f-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="25b8f-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="25b8f-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="25b8f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="25b8f-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="25b8f-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="25b8f-136">IID</span><span class="sxs-lookup"><span data-stu-id="25b8f-136">IID</span></span><br/>                      | <span data-ttu-id="25b8f-137">IID \_ IVMVirtualMachineCollection est défini en tant que 59f31786-2a3d-4FBF-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="25b8f-137">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25b8f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25b8f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25b8f-139">**IVMVirtualMachineCollection**</span><span class="sxs-lookup"><span data-stu-id="25b8f-139">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

