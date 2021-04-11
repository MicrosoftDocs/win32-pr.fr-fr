---
title: IVMVirtualNetworkCollection _NewEnum, propriété (VPCCOMInterfaces. h)
description: Récupère un énumérateur pour la collection. | IVMVirtualNetworkCollection _NewEnum, propriété (VPCCOMInterfaces. h)
ms.assetid: 3ea01a88-72ec-4dc0-901f-e48092cf9251
keywords:
- _NewEnum de la propriété Virtual PC
- _NewEnum propriété Virtual PC, interface IVMVirtualNetworkCollection
- IVMVirtualNetworkCollection interface Virtual PC, propriété _NewEnum
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection._NewEnum
- IVMVirtualNetworkCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b50a279e3f160a79f143a7516e29c0dbc3eccdf4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211638"
---
# <a name="ivmvirtualnetworkcollection_newenum-property"></a><span data-ttu-id="1d63e-107">IVMVirtualNetworkCollection :: \_ NewEnum, propriété</span><span class="sxs-lookup"><span data-stu-id="1d63e-107">IVMVirtualNetworkCollection::\_NewEnum property</span></span>

<span data-ttu-id="1d63e-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1d63e-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1d63e-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1d63e-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1d63e-110">Récupère un énumérateur pour la collection.</span><span class="sxs-lookup"><span data-stu-id="1d63e-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="1d63e-111">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1d63e-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d63e-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d63e-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="1d63e-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1d63e-113">Property value</span></span>

<span data-ttu-id="1d63e-114">Énumérateur [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="1d63e-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1d63e-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="1d63e-115">Error codes</span></span>



| <span data-ttu-id="1d63e-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="1d63e-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="1d63e-117">Signification</span><span class="sxs-lookup"><span data-stu-id="1d63e-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="1d63e-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1d63e-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="1d63e-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="1d63e-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="1d63e-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1d63e-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="1d63e-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1d63e-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="1d63e-122"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1d63e-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="1d63e-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1d63e-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1d63e-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d63e-124">Requirements</span></span>



| <span data-ttu-id="1d63e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d63e-125">Requirement</span></span> | <span data-ttu-id="1d63e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d63e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d63e-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d63e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1d63e-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d63e-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1d63e-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d63e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1d63e-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d63e-130">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1d63e-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1d63e-131">End of client support</span></span><br/>    | <span data-ttu-id="1d63e-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1d63e-132">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="1d63e-133">Produit</span><span class="sxs-lookup"><span data-stu-id="1d63e-133">Product</span></span><br/>                  | <span data-ttu-id="1d63e-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1d63e-134">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="1d63e-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d63e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d63e-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d63e-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="1d63e-137">IID</span><span class="sxs-lookup"><span data-stu-id="1d63e-137">IID</span></span><br/>                      | <span data-ttu-id="1d63e-138">IID \_ IVMVirtualNetworkCollection est défini en tant que 8ed680be-4242-4B2A-A21C-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="1d63e-138">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d63e-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d63e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d63e-140">**IVMVirtualNetworkCollection**</span><span class="sxs-lookup"><span data-stu-id="1d63e-140">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

