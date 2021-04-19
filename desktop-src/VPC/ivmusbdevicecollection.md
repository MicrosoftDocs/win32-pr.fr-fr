---
title: Interface IVMUSBDeviceCollection (VPCCOMInterfaces. h)
description: Définit la collection des périphériques USB attachés au système hôte. Pour obtenir un objet IVMUSBDeviceCollection, utilisez la propriété USBDeviceCollection IVMVirtualPC.
ms.assetid: a5cca485-29d3-47fa-9cda-fedcdc379155
keywords:
- Virtual PC de l’interface IVMUSBDeviceCollection
- IVMUSBDeviceCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e773f006a1d98253a20ad37d5a70db43f487980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509919"
---
# <a name="ivmusbdevicecollection-interface"></a><span data-ttu-id="18303-106">Interface IVMUSBDeviceCollection</span><span class="sxs-lookup"><span data-stu-id="18303-106">IVMUSBDeviceCollection interface</span></span>

<span data-ttu-id="18303-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="18303-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="18303-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="18303-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="18303-109">Définit la collection des périphériques USB attachés au système hôte.</span><span class="sxs-lookup"><span data-stu-id="18303-109">Defines the collection of USB devices attached to the host system.</span></span> <span data-ttu-id="18303-110">Pour obtenir un objet **IVMUSBDeviceCollection** , utilisez la propriété [**IVMVirtualPC :: USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) .</span><span class="sxs-lookup"><span data-stu-id="18303-110">To obtain an **IVMUSBDeviceCollection** object, use the [**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="18303-111">Membres</span><span class="sxs-lookup"><span data-stu-id="18303-111">Members</span></span>

<span data-ttu-id="18303-112">L’interface **IVMUSBDeviceCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="18303-112">The **IVMUSBDeviceCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="18303-113">**IVMUSBDeviceCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="18303-113">**IVMUSBDeviceCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="18303-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18303-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18303-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="18303-115">Properties</span></span>

<span data-ttu-id="18303-116">L’interface **IVMUSBDeviceCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="18303-116">The **IVMUSBDeviceCollection** interface has these properties.</span></span>



| <span data-ttu-id="18303-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="18303-117">Property</span></span>                                                        | <span data-ttu-id="18303-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="18303-118">Access type</span></span>          | <span data-ttu-id="18303-119">Description</span><span class="sxs-lookup"><span data-stu-id="18303-119">Description</span></span>                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="18303-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="18303-120">**\_NewEnum**</span></span>](ivmusbdevicecollection--newenum.md)<br/> | <span data-ttu-id="18303-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18303-121">Read-only</span></span><br/> | <span data-ttu-id="18303-122">Énumérateur de la collection.</span><span class="sxs-lookup"><span data-stu-id="18303-122">An enumerator for the collection.</span></span><br/>                                        |
| [<span data-ttu-id="18303-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="18303-123">**Count**</span></span>](ivmusbdevicecollection-count.md)<br/>        | <span data-ttu-id="18303-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18303-124">Read-only</span></span><br/> | <span data-ttu-id="18303-125">Nombre de périphériques USB dans ce regroupement.</span><span class="sxs-lookup"><span data-stu-id="18303-125">The number of USB devices in this collection.</span></span><br/>                            |
| [<span data-ttu-id="18303-126">**Élément**</span><span class="sxs-lookup"><span data-stu-id="18303-126">**Item**</span></span>](ivmusbdevicecollection-item.md)<br/>          | <span data-ttu-id="18303-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="18303-127">Read-only</span></span><br/> | <span data-ttu-id="18303-128">Objet périphérique USB qui correspond à l’index spécifié (basé sur 1).</span><span class="sxs-lookup"><span data-stu-id="18303-128">The USB device object that corresponds to the specified index (1-based).</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="18303-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18303-129">Requirements</span></span>



| <span data-ttu-id="18303-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18303-130">Requirement</span></span> | <span data-ttu-id="18303-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="18303-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="18303-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18303-132">Minimum supported client</span></span><br/> | <span data-ttu-id="18303-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18303-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="18303-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18303-134">Minimum supported server</span></span><br/> | <span data-ttu-id="18303-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="18303-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="18303-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="18303-136">End of client support</span></span><br/>    | <span data-ttu-id="18303-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="18303-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="18303-138">Produit</span><span class="sxs-lookup"><span data-stu-id="18303-138">Product</span></span><br/>                  | <span data-ttu-id="18303-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="18303-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="18303-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="18303-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="18303-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="18303-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="18303-142">IID</span><span class="sxs-lookup"><span data-stu-id="18303-142">IID</span></span><br/>                      | <span data-ttu-id="18303-143">IID \_ IVMUSBDeviceCollection est défini en tant que 4FBCD6A5-F53C-4D1C-9F4D-E90ABB8B3749</span><span class="sxs-lookup"><span data-stu-id="18303-143">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="18303-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18303-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18303-145">**IVMUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="18303-145">**IVMUSBDevice**</span></span>](ivmusbdevice.md)
</dt> <dt>

[<span data-ttu-id="18303-146">**IVMVirtualPC::USBDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="18303-146">**IVMVirtualPC::USBDeviceCollection**</span></span>](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

