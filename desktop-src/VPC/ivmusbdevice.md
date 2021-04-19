---
title: Interface IVMUSBDevice (VPCCOMInterfaces. h)
description: Définit l’interface pour un périphérique USB attaché à l’hôte. Vous pouvez attacher un périphérique USB à un ordinateur virtuel pour utiliser l’appareil à l’intérieur de la machine virtuelle.
ms.assetid: f491fe8f-bc43-4dfa-b9c1-c93b4e5a7df6
keywords:
- Virtual PC de l’interface IVMUSBDevice
- IVMUSBDevice interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1547bd812ea6d8f117f5910a254334676cafd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512809"
---
# <a name="ivmusbdevice-interface"></a><span data-ttu-id="58693-106">Interface IVMUSBDevice</span><span class="sxs-lookup"><span data-stu-id="58693-106">IVMUSBDevice interface</span></span>

<span data-ttu-id="58693-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="58693-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="58693-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="58693-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="58693-109">Définit l’interface pour un périphérique USB attaché à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="58693-109">Defines the interface for a USB device attached to host.</span></span> <span data-ttu-id="58693-110">Vous pouvez attacher un périphérique USB à un ordinateur virtuel pour utiliser l’appareil à l’intérieur de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="58693-110">You can attach USB device to a virtual machine to use the device inside the virtual machine.</span></span>

## <a name="members"></a><span data-ttu-id="58693-111">Membres</span><span class="sxs-lookup"><span data-stu-id="58693-111">Members</span></span>

<span data-ttu-id="58693-112">L’interface **IVMUSBDevice** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="58693-112">The **IVMUSBDevice** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="58693-113">**IVMUSBDevice** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="58693-113">**IVMUSBDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="58693-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="58693-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58693-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="58693-115">Properties</span></span>

<span data-ttu-id="58693-116">L’interface **IVMUSBDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="58693-116">The **IVMUSBDevice** interface has these properties.</span></span>



| <span data-ttu-id="58693-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="58693-117">Property</span></span>                                                                 | <span data-ttu-id="58693-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="58693-118">Access type</span></span>          | <span data-ttu-id="58693-119">Description</span><span class="sxs-lookup"><span data-stu-id="58693-119">Description</span></span>                                                                     |
|:-------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="58693-120">**AttachedToVM**</span><span class="sxs-lookup"><span data-stu-id="58693-120">**AttachedToVM**</span></span>](ivmusbdevice-attachedtovm.md)<br/>             | <span data-ttu-id="58693-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58693-121">Read-only</span></span><br/> | <span data-ttu-id="58693-122">Nom de la machine virtuelle à laquelle le périphérique USB est attaché.</span><span class="sxs-lookup"><span data-stu-id="58693-122">The name of the virtual machine to which the USB device is attached.</span></span><br/> |
| [<span data-ttu-id="58693-123">**DeviceClass**</span><span class="sxs-lookup"><span data-stu-id="58693-123">**DeviceClass**</span></span>](ivmusbdevice-deviceclass.md)<br/>               | <span data-ttu-id="58693-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58693-124">Read-only</span></span><br/> | <span data-ttu-id="58693-125">Classe de périphérique du périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="58693-125">The device class of the USB device.</span></span><br/>                                  |
| [<span data-ttu-id="58693-126">**DeviceString**</span><span class="sxs-lookup"><span data-stu-id="58693-126">**DeviceString**</span></span>](ivmusbdevice-devicestring.md)<br/>             | <span data-ttu-id="58693-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58693-127">Read-only</span></span><br/> | <span data-ttu-id="58693-128">Nom du périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="58693-128">The name of the USB device.</span></span><br/>                                          |
| [<span data-ttu-id="58693-129">**HubID**</span><span class="sxs-lookup"><span data-stu-id="58693-129">**HubID**</span></span>](ivmusbdevice-hubid.md)<br/>                           | <span data-ttu-id="58693-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58693-130">Read-only</span></span><br/> | <span data-ttu-id="58693-131">Identificateur du concentrateur sur lequel l’appareil est connecté.</span><span class="sxs-lookup"><span data-stu-id="58693-131">The identifier of the hub on which the device is connected.</span></span><br/>          |
| [<span data-ttu-id="58693-132">**ManufacturerString**</span><span class="sxs-lookup"><span data-stu-id="58693-132">**ManufacturerString**</span></span>](ivmusbdevice-manufacturerstring.md)<br/> | <span data-ttu-id="58693-133">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58693-133">Read-only</span></span><br/> | <span data-ttu-id="58693-134">Nom du fabricant du périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="58693-134">The name of the USB device manufacturer.</span></span><br/>                             |
| [<span data-ttu-id="58693-135">**Port**</span><span class="sxs-lookup"><span data-stu-id="58693-135">**Port**</span></span>](ivmusbdevice-port.md)<br/>                             | <span data-ttu-id="58693-136">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="58693-136">Read-only</span></span><br/> | <span data-ttu-id="58693-137">Identificateur du port sur lequel l’appareil est connecté.</span><span class="sxs-lookup"><span data-stu-id="58693-137">The identifier of the port on which the device is connected.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="58693-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58693-138">Requirements</span></span>



| <span data-ttu-id="58693-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58693-139">Requirement</span></span> | <span data-ttu-id="58693-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="58693-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="58693-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58693-141">Minimum supported client</span></span><br/> | <span data-ttu-id="58693-142">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58693-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="58693-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58693-143">Minimum supported server</span></span><br/> | <span data-ttu-id="58693-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="58693-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="58693-145">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="58693-145">End of client support</span></span><br/>    | <span data-ttu-id="58693-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="58693-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="58693-147">Produit</span><span class="sxs-lookup"><span data-stu-id="58693-147">Product</span></span><br/>                  | <span data-ttu-id="58693-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="58693-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="58693-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="58693-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="58693-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="58693-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="58693-151">IID</span><span class="sxs-lookup"><span data-stu-id="58693-151">IID</span></span><br/>                      | <span data-ttu-id="58693-152">IID \_ IVMUSBDevice est défini en tant que 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span><span class="sxs-lookup"><span data-stu-id="58693-152">IID\_IVMUSBDevice is defined as 63C1258C-5721-4070-B86B-A6CE2AFEC0B3</span></span><br/>               |



 

