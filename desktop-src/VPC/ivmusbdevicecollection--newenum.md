---
title: IVMUSBDeviceCollection _NewEnum, propriété (VPCCOMInterfaces. h)
description: Récupère un énumérateur pour la collection. | IVMUSBDeviceCollection _NewEnum, propriété (VPCCOMInterfaces. h)
ms.assetid: f14f64a0-e65a-44d6-b053-54bbcb9ea804
keywords:
- _NewEnum de la propriété Virtual PC
- _NewEnum propriété Virtual PC, interface IVMUSBDeviceCollection
- IVMUSBDeviceCollection interface Virtual PC, propriété _NewEnum
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection._NewEnum
- IVMUSBDeviceCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e1e2a4d80691be26161ae4835ccb85c0e722d8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103953772"
---
# <a name="ivmusbdevicecollection_newenum-property"></a><span data-ttu-id="d1ed6-107">IVMUSBDeviceCollection :: \_ NewEnum, propriété</span><span class="sxs-lookup"><span data-stu-id="d1ed6-107">IVMUSBDeviceCollection::\_NewEnum property</span></span>

<span data-ttu-id="d1ed6-108">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d1ed6-109">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d1ed6-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d1ed6-110">Récupère un énumérateur pour la collection.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="d1ed6-111">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1ed6-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1ed6-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="d1ed6-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d1ed6-113">Property value</span></span>

<span data-ttu-id="d1ed6-114">Énumérateur [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="d1ed6-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d1ed6-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d1ed6-115">Error codes</span></span>



| <span data-ttu-id="d1ed6-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="d1ed6-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d1ed6-117">Signification</span><span class="sxs-lookup"><span data-stu-id="d1ed6-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d1ed6-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d1ed6-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d1ed6-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="d1ed6-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d1ed6-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d1ed6-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="d1ed6-122"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d1ed6-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d1ed6-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d1ed6-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d1ed6-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1ed6-124">Requirements</span></span>



| <span data-ttu-id="d1ed6-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1ed6-125">Requirement</span></span> | <span data-ttu-id="d1ed6-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1ed6-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ed6-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1ed6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d1ed6-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1ed6-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1ed6-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1ed6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d1ed6-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1ed6-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d1ed6-131">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d1ed6-131">End of client support</span></span><br/>    | <span data-ttu-id="d1ed6-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d1ed6-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d1ed6-133">Produit</span><span class="sxs-lookup"><span data-stu-id="d1ed6-133">Product</span></span><br/>                  | <span data-ttu-id="d1ed6-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d1ed6-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d1ed6-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1ed6-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1ed6-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1ed6-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d1ed6-137">IID</span><span class="sxs-lookup"><span data-stu-id="d1ed6-137">IID</span></span><br/>                      | <span data-ttu-id="d1ed6-138">IID \_ IVMUSBDeviceCollection est défini en tant que 4FBCD6A5-F53C-4D1C-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="d1ed6-138">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="d1ed6-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1ed6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1ed6-140">**IVMUSBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="d1ed6-140">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

