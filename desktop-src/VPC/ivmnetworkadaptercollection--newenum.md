---
title: IVMNetworkAdapterCollection _NewEnum, propriété (VPCCOMInterfaces. h)
description: Récupère un énumérateur pour la collection. | IVMNetworkAdapterCollection _NewEnum, propriété (VPCCOMInterfaces. h)
ms.assetid: 9b970fc6-f8a3-4a16-9d59-789a59a99b68
keywords:
- _NewEnum de la propriété Virtual PC
- _NewEnum propriété Virtual PC, interface IVMNetworkAdapterCollection
- IVMNetworkAdapterCollection interface Virtual PC, propriété _NewEnum
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection._NewEnum
- IVMNetworkAdapterCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf118700a81865ff93ee581cbb2efd07d237805
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106541247"
---
# <a name="ivmnetworkadaptercollection_newenum-property"></a><span data-ttu-id="18a95-107">IVMNetworkAdapterCollection :: \_ NewEnum, propriété</span><span class="sxs-lookup"><span data-stu-id="18a95-107">IVMNetworkAdapterCollection::\_NewEnum property</span></span>

<span data-ttu-id="18a95-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="18a95-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="18a95-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="18a95-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="18a95-110">Récupère un énumérateur pour la collection.</span><span class="sxs-lookup"><span data-stu-id="18a95-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="18a95-111">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="18a95-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="18a95-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18a95-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="18a95-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="18a95-113">Property value</span></span>

<span data-ttu-id="18a95-114">Énumérateur [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="18a95-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="18a95-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="18a95-115">Error codes</span></span>



| <span data-ttu-id="18a95-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="18a95-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="18a95-117">Signification</span><span class="sxs-lookup"><span data-stu-id="18a95-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="18a95-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="18a95-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="18a95-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="18a95-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="18a95-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="18a95-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="18a95-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="18a95-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="18a95-122"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="18a95-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="18a95-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="18a95-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="18a95-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18a95-124">Requirements</span></span>



| <span data-ttu-id="18a95-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18a95-125">Requirement</span></span> | <span data-ttu-id="18a95-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="18a95-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18a95-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18a95-127">Minimum supported client</span></span><br/> | <span data-ttu-id="18a95-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18a95-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="18a95-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18a95-129">Minimum supported server</span></span><br/> | <span data-ttu-id="18a95-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="18a95-130">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="18a95-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="18a95-131">End of client support</span></span><br/>    | <span data-ttu-id="18a95-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="18a95-132">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="18a95-133">Produit</span><span class="sxs-lookup"><span data-stu-id="18a95-133">Product</span></span><br/>                  | <span data-ttu-id="18a95-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="18a95-134">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="18a95-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="18a95-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="18a95-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="18a95-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="18a95-137">IID</span><span class="sxs-lookup"><span data-stu-id="18a95-137">IID</span></span><br/>                      | <span data-ttu-id="18a95-138">IID \_ IVMNetworkAdapterCollection est défini en tant que ebaeafe9-EBCD-47cf-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="18a95-138">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="18a95-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18a95-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18a95-140">**IVMNetworkAdapterCollection**</span><span class="sxs-lookup"><span data-stu-id="18a95-140">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

