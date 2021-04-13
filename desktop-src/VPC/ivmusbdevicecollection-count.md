---
title: Propriété Count IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Récupère le nombre de périphériques USB de cette collection.
ms.assetid: 8d17397b-4f4a-475d-99fe-4df0d74fe5a5
keywords:
- Propriété Count Virtual PC
- Propriété Count Virtual PC, IVMUSBDeviceCollection, interface
- IVMUSBDeviceCollection interface Virtual PC, propriété Count
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Count
- IVMUSBDeviceCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a0c2146df70f0432a19d65daad44ba6f1ec372
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465530"
---
# <a name="ivmusbdevicecollectioncount-property"></a><span data-ttu-id="c9d56-106">IVMUSBDeviceCollection :: Count, propriété</span><span class="sxs-lookup"><span data-stu-id="c9d56-106">IVMUSBDeviceCollection::Count property</span></span>

<span data-ttu-id="c9d56-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c9d56-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c9d56-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c9d56-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c9d56-109">Récupère le nombre de périphériques USB de cette collection.</span><span class="sxs-lookup"><span data-stu-id="c9d56-109">Retrieves the number of USB devices in this collection.</span></span>

<span data-ttu-id="c9d56-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c9d56-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d56-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9d56-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="c9d56-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c9d56-112">Property value</span></span>

<span data-ttu-id="c9d56-113">Nombre de périphériques USB.</span><span class="sxs-lookup"><span data-stu-id="c9d56-113">The number of USB devices.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c9d56-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c9d56-114">Error codes</span></span>



| <span data-ttu-id="c9d56-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="c9d56-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c9d56-116">Signification</span><span class="sxs-lookup"><span data-stu-id="c9d56-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c9d56-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c9d56-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c9d56-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c9d56-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c9d56-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c9d56-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c9d56-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c9d56-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="c9d56-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c9d56-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c9d56-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c9d56-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c9d56-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9d56-123">Requirements</span></span>



| <span data-ttu-id="c9d56-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9d56-124">Requirement</span></span> | <span data-ttu-id="c9d56-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9d56-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d56-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9d56-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c9d56-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9d56-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9d56-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9d56-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c9d56-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9d56-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c9d56-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c9d56-130">End of client support</span></span><br/>    | <span data-ttu-id="c9d56-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c9d56-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c9d56-132">Produit</span><span class="sxs-lookup"><span data-stu-id="c9d56-132">Product</span></span><br/>                  | <span data-ttu-id="c9d56-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c9d56-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c9d56-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9d56-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9d56-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9d56-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c9d56-136">IID</span><span class="sxs-lookup"><span data-stu-id="c9d56-136">IID</span></span><br/>                      | <span data-ttu-id="c9d56-137">IID \_ IVMUSBDeviceCollection est défini en tant que 4FBCD6A5-F53C-4D1C-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="c9d56-137">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="c9d56-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9d56-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d56-139">**IVMUSBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="c9d56-139">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

