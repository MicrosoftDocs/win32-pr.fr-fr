---
title: IVMVirtualPC USBDeviceCollection, propriété (VPCCOMInterfaces. h)
description: Collection énumérable de tous les périphériques USB connectés à l’hôte.
ms.assetid: 80844912-15b1-44d1-8d07-dca90c579927
keywords:
- USBDeviceCollection propriété Virtual PC
- USBDeviceCollection, propriété Virtual PC, IVMVirtualPC, interface
- IVMVirtualPC interface Virtual PC, propriété USBDeviceCollection
topic_type:
- apiref
api_name:
- IVMVirtualPC.USBDeviceCollection
- IVMVirtualPC.get_USBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0428862cdd53ef6e657624d5dbd3e15c2445042f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742037"
---
# <a name="ivmvirtualpcusbdevicecollection-property"></a><span data-ttu-id="4d7ab-106">IVMVirtualPC :: USBDeviceCollection, propriété</span><span class="sxs-lookup"><span data-stu-id="4d7ab-106">IVMVirtualPC::USBDeviceCollection property</span></span>

<span data-ttu-id="4d7ab-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4d7ab-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4d7ab-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4d7ab-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4d7ab-109">Récupère une collection énumérable de tous les périphériques USB connectés à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="4d7ab-109">Retrieves an enumerable collection of all USB devices connected to the host.</span></span>

<span data-ttu-id="4d7ab-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4d7ab-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7ab-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d7ab-111">Syntax</span></span>


```C++
HRESULT get_USBDeviceCollection(
  [out, retval] IVMUSBDeviceCollection **usbDeviceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="4d7ab-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4d7ab-112">Property value</span></span>

<span data-ttu-id="4d7ab-113">Référence à un pointeur [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md) qui représente une collection d’objets [**IVMUSBDevice**](ivmusbdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="4d7ab-113">A reference to an [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md) pointer that represents a collection of [**IVMUSBDevice**](ivmusbdevice.md) objects.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4d7ab-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4d7ab-114">Error codes</span></span>



| <span data-ttu-id="4d7ab-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="4d7ab-115">Name/value</span></span>                                                                                                                                                                                | <span data-ttu-id="4d7ab-116">Signification</span><span class="sxs-lookup"><span data-stu-id="4d7ab-116">Meaning</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d7ab-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4d7ab-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                   | <span data-ttu-id="4d7ab-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4d7ab-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4d7ab-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4d7ab-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                     | <span data-ttu-id="4d7ab-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4d7ab-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="4d7ab-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4d7ab-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                             | <span data-ttu-id="4d7ab-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="4d7ab-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="4d7ab-123"><dt>Ordinateur virtuel \_ Échec de l' \_ énumération E USB- \_ nombre d' \_ \_ \_ appareils</dt> <dt>0xA0040930</dt></span><span class="sxs-lookup"><span data-stu-id="4d7ab-123"><dt>VM\_E\_USB\_ENUMERATION\_FAILED\_MORE\_DEVICES</dt> <dt>0xA0040930</dt></span></span> </dl> | <span data-ttu-id="4d7ab-124">Plus de 16 périphériques USB sont connectés à l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="4d7ab-124">More than 16 USB devices are connected to the host.</span></span><br/>                                  |
| <dl> <span data-ttu-id="4d7ab-125"><dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="4d7ab-125"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>      | <span data-ttu-id="4d7ab-126">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="4d7ab-126">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4d7ab-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d7ab-127">Requirements</span></span>



| <span data-ttu-id="4d7ab-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d7ab-128">Requirement</span></span> | <span data-ttu-id="4d7ab-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d7ab-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7ab-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d7ab-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4d7ab-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4d7ab-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4d7ab-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d7ab-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4d7ab-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d7ab-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4d7ab-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4d7ab-134">End of client support</span></span><br/>    | <span data-ttu-id="4d7ab-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d7ab-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4d7ab-136">Produit</span><span class="sxs-lookup"><span data-stu-id="4d7ab-136">Product</span></span><br/>                  | <span data-ttu-id="4d7ab-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4d7ab-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4d7ab-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d7ab-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d7ab-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d7ab-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4d7ab-140">IID</span><span class="sxs-lookup"><span data-stu-id="4d7ab-140">IID</span></span><br/>                      | <span data-ttu-id="4d7ab-141">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="4d7ab-141">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="4d7ab-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d7ab-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d7ab-143">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="4d7ab-143">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

