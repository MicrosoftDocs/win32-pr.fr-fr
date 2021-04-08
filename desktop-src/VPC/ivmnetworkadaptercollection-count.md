---
title: Propriété Count IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Récupère le nombre d’interfaces réseau de cette collection.
ms.assetid: 0b6391fa-62fe-4db1-b0a2-565ab17157ab
keywords:
- Propriété Count Virtual PC
- Propriété Count Virtual PC, IVMNetworkAdapterCollection, interface
- IVMNetworkAdapterCollection interface Virtual PC, propriété Count
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Count
- IVMNetworkAdapterCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a287122d9829cd98f355d44e6bd408f6ca0d67a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102805"
---
# <a name="ivmnetworkadaptercollectioncount-property"></a><span data-ttu-id="c8795-106">IVMNetworkAdapterCollection :: Count, propriété</span><span class="sxs-lookup"><span data-stu-id="c8795-106">IVMNetworkAdapterCollection::Count property</span></span>

<span data-ttu-id="c8795-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c8795-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c8795-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c8795-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c8795-109">Récupère le nombre d’interfaces réseau de cette collection.</span><span class="sxs-lookup"><span data-stu-id="c8795-109">Retrieves the number of network interfaces in this collection.</span></span>

<span data-ttu-id="c8795-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c8795-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8795-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8795-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="c8795-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c8795-112">Property value</span></span>

<span data-ttu-id="c8795-113">Nombre d’interfaces réseau.</span><span class="sxs-lookup"><span data-stu-id="c8795-113">The number of network interfaces.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c8795-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c8795-114">Error codes</span></span>



| <span data-ttu-id="c8795-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="c8795-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c8795-116">Signification</span><span class="sxs-lookup"><span data-stu-id="c8795-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c8795-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8795-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c8795-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c8795-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c8795-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c8795-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c8795-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c8795-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="c8795-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c8795-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c8795-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c8795-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c8795-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8795-123">Requirements</span></span>



| <span data-ttu-id="c8795-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8795-124">Requirement</span></span> | <span data-ttu-id="c8795-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8795-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8795-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8795-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c8795-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8795-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c8795-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8795-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c8795-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8795-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c8795-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c8795-130">End of client support</span></span><br/>    | <span data-ttu-id="c8795-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8795-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="c8795-132">Produit</span><span class="sxs-lookup"><span data-stu-id="c8795-132">Product</span></span><br/>                  | <span data-ttu-id="c8795-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c8795-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="c8795-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8795-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8795-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8795-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="c8795-136">IID</span><span class="sxs-lookup"><span data-stu-id="c8795-136">IID</span></span><br/>                      | <span data-ttu-id="c8795-137">IID \_ IVMNetworkAdapterCollection est défini en tant que ebaeafe9-EBCD-47cf-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="c8795-137">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8795-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8795-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8795-139">**IVMNetworkAdapterCollection**</span><span class="sxs-lookup"><span data-stu-id="c8795-139">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

