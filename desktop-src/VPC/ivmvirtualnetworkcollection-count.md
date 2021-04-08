---
title: Propriété Count IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Récupère le nombre de réseaux virtuels de ce regroupement.
ms.assetid: a9a3ab48-74a0-498e-936e-a99c7b027a85
keywords:
- Propriété Count Virtual PC
- Propriété Count Virtual PC, IVMVirtualNetworkCollection, interface
- IVMVirtualNetworkCollection interface Virtual PC, propriété Count
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Count
- IVMVirtualNetworkCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82e3244327d5840c8f7cce8ed498f90cd406d573
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742733"
---
# <a name="ivmvirtualnetworkcollectioncount-property"></a><span data-ttu-id="7cc57-106">IVMVirtualNetworkCollection :: Count, propriété</span><span class="sxs-lookup"><span data-stu-id="7cc57-106">IVMVirtualNetworkCollection::Count property</span></span>

<span data-ttu-id="7cc57-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7cc57-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7cc57-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7cc57-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7cc57-109">Récupère le nombre de réseaux virtuels de ce regroupement.</span><span class="sxs-lookup"><span data-stu-id="7cc57-109">Retrieves the number of virtual networks in this collection.</span></span>

<span data-ttu-id="7cc57-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7cc57-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cc57-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cc57-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="7cc57-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7cc57-112">Property value</span></span>

<span data-ttu-id="7cc57-113">Nombre de réseaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="7cc57-113">The number of virtual networks.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7cc57-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7cc57-114">Error codes</span></span>



| <span data-ttu-id="7cc57-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="7cc57-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7cc57-116">Signification</span><span class="sxs-lookup"><span data-stu-id="7cc57-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7cc57-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7cc57-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7cc57-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="7cc57-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="7cc57-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7cc57-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7cc57-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7cc57-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="7cc57-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7cc57-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7cc57-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="7cc57-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7cc57-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cc57-123">Requirements</span></span>



| <span data-ttu-id="7cc57-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cc57-124">Requirement</span></span> | <span data-ttu-id="7cc57-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cc57-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cc57-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cc57-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7cc57-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cc57-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7cc57-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cc57-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7cc57-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cc57-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7cc57-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7cc57-130">End of client support</span></span><br/>    | <span data-ttu-id="7cc57-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7cc57-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="7cc57-132">Produit</span><span class="sxs-lookup"><span data-stu-id="7cc57-132">Product</span></span><br/>                  | <span data-ttu-id="7cc57-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7cc57-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="7cc57-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="7cc57-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cc57-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cc57-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="7cc57-136">IID</span><span class="sxs-lookup"><span data-stu-id="7cc57-136">IID</span></span><br/>                      | <span data-ttu-id="7cc57-137">IID \_ IVMVirtualNetworkCollection est défini en tant que 8ed680be-4242-4B2A-A21C-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="7cc57-137">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7cc57-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cc57-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cc57-139">**IVMVirtualNetworkCollection**</span><span class="sxs-lookup"><span data-stu-id="7cc57-139">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

