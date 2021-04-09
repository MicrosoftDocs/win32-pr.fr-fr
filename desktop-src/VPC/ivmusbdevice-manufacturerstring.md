---
title: IVMUSBDevice ManufacturerString, propriété (VPCCOMInterfaces. h)
description: Récupère le nom du fabricant du périphérique USB.
ms.assetid: 0d815887-96bf-4795-a4eb-32fb2f35c57e
keywords:
- ManufacturerString propriété Virtual PC
- ManufacturerString, propriété Virtual PC, IVMUSBDevice, interface
- IVMUSBDevice interface Virtual PC, propriété ManufacturerString
topic_type:
- apiref
api_name:
- IVMUSBDevice.ManufacturerString
- IVMUSBDevice.get_ManufacturerString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8d74cbe737c59e10daf2cf3ee93e4b1f14983f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104911"
---
# <a name="ivmusbdevicemanufacturerstring-property"></a><span data-ttu-id="9b49c-106">IVMUSBDevice :: ManufacturerString, propriété</span><span class="sxs-lookup"><span data-stu-id="9b49c-106">IVMUSBDevice::ManufacturerString property</span></span>

<span data-ttu-id="9b49c-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9b49c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9b49c-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9b49c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9b49c-109">Récupère le nom du fabricant du périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="9b49c-109">Retrieves the name of the USB device manufacturer.</span></span>

<span data-ttu-id="9b49c-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9b49c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b49c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b49c-111">Syntax</span></span>


```C++
HRESULT get_ManufacturerString(
  [out, retval] BSTR *manufacturerName
);
```



## <a name="property-value"></a><span data-ttu-id="9b49c-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9b49c-112">Property value</span></span>

<span data-ttu-id="9b49c-113">Nom du fabricant du périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="9b49c-113">The name of the USB device manufacturer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9b49c-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9b49c-114">Error codes</span></span>



| <span data-ttu-id="9b49c-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="9b49c-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="9b49c-116">Signification</span><span class="sxs-lookup"><span data-stu-id="9b49c-116">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="9b49c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9b49c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="9b49c-118">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="9b49c-118">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="9b49c-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9b49c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="9b49c-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="9b49c-120">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="9b49c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b49c-121">Requirements</span></span>



| <span data-ttu-id="9b49c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b49c-122">Requirement</span></span> | <span data-ttu-id="9b49c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b49c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b49c-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b49c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9b49c-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b49c-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9b49c-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b49c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9b49c-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b49c-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9b49c-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9b49c-128">End of client support</span></span><br/>    | <span data-ttu-id="9b49c-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b49c-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9b49c-130">Produit</span><span class="sxs-lookup"><span data-stu-id="9b49c-130">Product</span></span><br/>                  | <span data-ttu-id="9b49c-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9b49c-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9b49c-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b49c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b49c-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b49c-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9b49c-134">IID</span><span class="sxs-lookup"><span data-stu-id="9b49c-134">IID</span></span><br/>                      | <span data-ttu-id="9b49c-135">IID \_ IVMUSBDevice est défini en tant que 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="9b49c-135">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9b49c-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b49c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b49c-137">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="9b49c-137">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

