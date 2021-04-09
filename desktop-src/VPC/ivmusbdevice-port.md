---
title: Propriété de port IVMUSBDevice (VPCCOMInterfaces. h)
description: Récupère l’identificateur du port sur lequel l’appareil est connecté.
ms.assetid: 612c0eba-aa80-4539-a883-f05d32d13b41
keywords:
- Propriété de port Virtual PC
- Propriété de port Virtual PC, interface IVMUSBDevice
- IVMUSBDevice interface Virtual PC, propriété Port
topic_type:
- apiref
api_name:
- IVMUSBDevice.Port
- IVMUSBDevice.get_Port
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb821921d10b23fdb17256372708650d060e253b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743237"
---
# <a name="ivmusbdeviceport-property"></a><span data-ttu-id="9b18c-106">IVMUSBDevice ::P (propriété)</span><span class="sxs-lookup"><span data-stu-id="9b18c-106">IVMUSBDevice::Port property</span></span>

<span data-ttu-id="9b18c-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9b18c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9b18c-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9b18c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9b18c-109">Récupère l’identificateur du port sur lequel l’appareil est connecté.</span><span class="sxs-lookup"><span data-stu-id="9b18c-109">Retrieves the identifier of the port on which the device is connected.</span></span>

<span data-ttu-id="9b18c-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9b18c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b18c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b18c-111">Syntax</span></span>


```C++
HRESULT get_Port(
  [out, retval] long *port
);
```



## <a name="property-value"></a><span data-ttu-id="9b18c-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9b18c-112">Property value</span></span>

<span data-ttu-id="9b18c-113">Identificateur du port.</span><span class="sxs-lookup"><span data-stu-id="9b18c-113">The port identifier.</span></span> <span data-ttu-id="9b18c-114">Cette valeur est affectée par le pilote du connecteur USB.</span><span class="sxs-lookup"><span data-stu-id="9b18c-114">This value is assigned by the USB connector driver.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9b18c-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9b18c-115">Error codes</span></span>



| <span data-ttu-id="9b18c-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="9b18c-116">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="9b18c-117">Signification</span><span class="sxs-lookup"><span data-stu-id="9b18c-117">Meaning</span></span>                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="9b18c-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9b18c-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="9b18c-119">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="9b18c-119">The method completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="9b18c-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9b18c-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="9b18c-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="9b18c-121">The parameter is **NULL**.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="9b18c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b18c-122">Requirements</span></span>



| <span data-ttu-id="9b18c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b18c-123">Requirement</span></span> | <span data-ttu-id="9b18c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b18c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b18c-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b18c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9b18c-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b18c-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9b18c-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b18c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9b18c-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b18c-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9b18c-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9b18c-129">End of client support</span></span><br/>    | <span data-ttu-id="9b18c-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b18c-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9b18c-131">Produit</span><span class="sxs-lookup"><span data-stu-id="9b18c-131">Product</span></span><br/>                  | <span data-ttu-id="9b18c-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9b18c-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9b18c-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b18c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b18c-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b18c-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9b18c-135">IID</span><span class="sxs-lookup"><span data-stu-id="9b18c-135">IID</span></span><br/>                      | <span data-ttu-id="9b18c-136">IID \_ IVMUSBDevice est défini en tant que 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="9b18c-136">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9b18c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b18c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b18c-138">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="9b18c-138">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> </dl>

 

