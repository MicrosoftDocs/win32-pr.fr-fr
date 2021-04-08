---
title: IVMUSBDevice HubID, propriété (VPCCOMInterfaces. h)
description: Récupère l’identificateur du concentrateur sur lequel l’appareil est connecté.
ms.assetid: 22e1d8fb-33f4-43a3-883f-174ddafa17c2
keywords:
- HubID propriété Virtual PC
- HubID, propriété Virtual PC, IVMUSBDevice, interface
- IVMUSBDevice interface Virtual PC, propriété HubID
topic_type:
- apiref
api_name:
- IVMUSBDevice.HubID
- IVMUSBDevice.get_HubID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53faa79ee999022f993070767846ee4e4723c3a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033068"
---
# <a name="ivmusbdevicehubid-property"></a><span data-ttu-id="27975-106">IVMUSBDevice :: HubID, propriété</span><span class="sxs-lookup"><span data-stu-id="27975-106">IVMUSBDevice::HubID property</span></span>

<span data-ttu-id="27975-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="27975-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="27975-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="27975-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="27975-109">Récupère l’identificateur du concentrateur sur lequel l’appareil est connecté.</span><span class="sxs-lookup"><span data-stu-id="27975-109">Retrieves the identifier of the hub on which the device is connected.</span></span>

<span data-ttu-id="27975-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="27975-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="27975-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="27975-111">Syntax</span></span>


```C++
HRESULT get_HubID(
  [out, retval] long *hubID
);
```



## <a name="property-value"></a><span data-ttu-id="27975-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="27975-112">Property value</span></span>

<span data-ttu-id="27975-113">Identificateur du concentrateur.</span><span class="sxs-lookup"><span data-stu-id="27975-113">The hub identifier.</span></span> <span data-ttu-id="27975-114">Cette valeur est affectée par le pilote du connecteur USB.</span><span class="sxs-lookup"><span data-stu-id="27975-114">This value is assigned by the USB connector driver.</span></span>

## <a name="error-codes"></a><span data-ttu-id="27975-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="27975-115">Error codes</span></span>



| <span data-ttu-id="27975-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="27975-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="27975-117">Signification</span><span class="sxs-lookup"><span data-stu-id="27975-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="27975-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="27975-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="27975-119">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="27975-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="27975-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="27975-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="27975-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="27975-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="27975-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27975-122">Requirements</span></span>



| <span data-ttu-id="27975-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27975-123">Requirement</span></span> | <span data-ttu-id="27975-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="27975-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="27975-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27975-125">Minimum supported client</span></span><br/> | <span data-ttu-id="27975-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27975-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27975-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27975-127">Minimum supported server</span></span><br/> | <span data-ttu-id="27975-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="27975-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="27975-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="27975-129">End of client support</span></span><br/>    | <span data-ttu-id="27975-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="27975-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="27975-131">Produit</span><span class="sxs-lookup"><span data-stu-id="27975-131">Product</span></span><br/>                  | <span data-ttu-id="27975-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="27975-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="27975-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="27975-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="27975-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="27975-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="27975-135">IID</span><span class="sxs-lookup"><span data-stu-id="27975-135">IID</span></span><br/>                      | <span data-ttu-id="27975-136">IID \_ IVMUSBDevice est défini en tant que 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="27975-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="27975-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27975-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27975-138">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="27975-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

