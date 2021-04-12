---
title: IVMUSBDevice DeviceClass, propriété (VPCCOMInterfaces. h)
description: Récupère la classe de périphérique du périphérique USB.
ms.assetid: 46c258b9-6064-4e8c-aa5d-71b26c07351c
keywords:
- DeviceClass propriété Virtual PC
- DeviceClass, propriété Virtual PC, IVMUSBDevice, interface
- IVMUSBDevice interface Virtual PC, propriété DeviceClass
topic_type:
- apiref
api_name:
- IVMUSBDevice.DeviceClass
- IVMUSBDevice.get_DeviceClass
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b758092763c95c4443caeaca3f50be08e31c112c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385040"
---
# <a name="ivmusbdevicedeviceclass-property"></a><span data-ttu-id="d08db-106">IVMUSBDevice ::D propriété eviceClass</span><span class="sxs-lookup"><span data-stu-id="d08db-106">IVMUSBDevice::DeviceClass property</span></span>

<span data-ttu-id="d08db-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d08db-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d08db-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d08db-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d08db-109">Récupère la classe de périphérique du périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="d08db-109">Retrieves the device class of the USB device.</span></span>

<span data-ttu-id="d08db-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d08db-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d08db-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d08db-111">Syntax</span></span>


```C++
HRESULT get_DeviceClass(
  [out, retval] VMUSBDeviceClassEnum *deviceClass
);
```



## <a name="property-value"></a><span data-ttu-id="d08db-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d08db-112">Property value</span></span>

<span data-ttu-id="d08db-113">Classe de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d08db-113">The device class.</span></span> <span data-ttu-id="d08db-114">Pour obtenir la liste des valeurs, consultez [**VMUSBDeviceClassEnum**](vmusbdeviceclassenum.md).</span><span class="sxs-lookup"><span data-stu-id="d08db-114">For a list of values, see [**VMUSBDeviceClassEnum**](vmusbdeviceclassenum.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="d08db-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d08db-115">Error codes</span></span>



| <span data-ttu-id="d08db-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="d08db-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="d08db-117">Signification</span><span class="sxs-lookup"><span data-stu-id="d08db-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="d08db-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d08db-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="d08db-119">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="d08db-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="d08db-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d08db-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="d08db-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d08db-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="d08db-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d08db-122">Requirements</span></span>



| <span data-ttu-id="d08db-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d08db-123">Requirement</span></span> | <span data-ttu-id="d08db-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d08db-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d08db-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d08db-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d08db-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d08db-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d08db-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d08db-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d08db-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d08db-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d08db-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d08db-129">End of client support</span></span><br/>    | <span data-ttu-id="d08db-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d08db-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d08db-131">Produit</span><span class="sxs-lookup"><span data-stu-id="d08db-131">Product</span></span><br/>                  | <span data-ttu-id="d08db-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d08db-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d08db-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="d08db-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d08db-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d08db-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d08db-135">IID</span><span class="sxs-lookup"><span data-stu-id="d08db-135">IID</span></span><br/>                      | <span data-ttu-id="d08db-136">IID \_ IVMUSBDevice est défini en tant que 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="d08db-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d08db-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d08db-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d08db-138">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="d08db-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

