---
title: Énumération VMUSBDeviceClassEnum (VPCCOMInterfaces. h)
description: Spécifie la classe de périphérique USB.
ms.assetid: 3f5044ea-f7a4-4524-bfb8-55db22732f81
keywords:
- Virtual PC de l’énumération VMUSBDeviceClassEnum
topic_type:
- apiref
api_name:
- VMUSBDeviceClassEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70335ae083ac2a80717ae64cc8c76f0aff9e791b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104902"
---
# <a name="vmusbdeviceclassenum-enumeration"></a><span data-ttu-id="f897d-104">Énumération VMUSBDeviceClassEnum</span><span class="sxs-lookup"><span data-stu-id="f897d-104">VMUSBDeviceClassEnum enumeration</span></span>

<span data-ttu-id="f897d-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f897d-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f897d-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f897d-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f897d-107">Spécifie la classe de périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="f897d-107">Specifies the USB device class.</span></span>

## <a name="syntax"></a><span data-ttu-id="f897d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f897d-108">Syntax</span></span>


```C++
typedef enum  { 
  vmUSBDeviceClass_InterfaceDescriptor  = 0x00,
  vmUSBDeviceClass_Audio                = 0x01,
  vmUSBDeviceClass_Communication        = 0x02,
  vmUSBDeviceClass_HID                  = 0x03,
  vmUSBDeviceClass_Physical             = 0x05,
  vmUSBDeviceClass_Image                = 0x06,
  vmUSBDeviceClass_Printer              = 0x07,
  vmUSBDeviceClass_MassStorage          = 0x08,
  vmUSBDeviceClass_Hub                  = 0x09,
  vmUSBDeviceClass_CDCData              = 0x0A,
  vmUSBDeviceClass_SmartCard            = 0x0B,
  vmUSBDeviceClass_ContentSecurity      = 0x0D,
  vmUSBDeviceClass_Video                = 0x0E,
  vmUSBDeviceClass_PersonalHealthcare   = 0x0F,
  vmUSBDeviceClass_DiagnosticDevice     = 0xDC,
  vmUSBDeviceClass_WirelessController   = 0xE0,
  vmUSBDeviceClass_Miscellaneous        = 0xEF,
  vmUSBDeviceClass_ApplicationSpecific  = 0xFE,
  vmUSBDeviceClass_VendorSpecific       = 0xFF
} VMUSBDeviceClassEnum;
```



## <a name="constants"></a><span data-ttu-id="f897d-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="f897d-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f897d-110"><span id="vmUSBDeviceClass_InterfaceDescriptor"></span><span id="vmusbdeviceclass_interfacedescriptor"></span><span id="VMUSBDEVICECLASS_INTERFACEDESCRIPTOR"></span>**vmUSBDeviceClass \_ InterfaceDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f897d-110"><span id="vmUSBDeviceClass_InterfaceDescriptor"></span><span id="vmusbdeviceclass_interfacedescriptor"></span><span id="VMUSBDEVICECLASS_INTERFACEDESCRIPTOR"></span>**vmUSBDeviceClass\_InterfaceDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-111">Appareil non identifié.</span><span class="sxs-lookup"><span data-stu-id="f897d-111">An unidentified device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-112"><span id="vmUSBDeviceClass_Audio"></span><span id="vmusbdeviceclass_audio"></span><span id="VMUSBDEVICECLASS_AUDIO"></span>**vmUSBDeviceClass \_ audio**</span><span class="sxs-lookup"><span data-stu-id="f897d-112"><span id="vmUSBDeviceClass_Audio"></span><span id="vmusbdeviceclass_audio"></span><span id="VMUSBDEVICECLASS_AUDIO"></span>**vmUSBDeviceClass\_Audio**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-113">Périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="f897d-113">Audio device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-114"><span id="vmUSBDeviceClass_Communication"></span><span id="vmusbdeviceclass_communication"></span><span id="VMUSBDEVICECLASS_COMMUNICATION"></span>**\_communication vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="f897d-114"><span id="vmUSBDeviceClass_Communication"></span><span id="vmusbdeviceclass_communication"></span><span id="VMUSBDEVICECLASS_COMMUNICATION"></span>**vmUSBDeviceClass\_Communication**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-115">Appareil de communication.</span><span class="sxs-lookup"><span data-stu-id="f897d-115">Communication device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-116"><span id="vmUSBDeviceClass_HID"></span><span id="vmusbdeviceclass_hid"></span><span id="VMUSBDEVICECLASS_HID"></span>**\_HID vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="f897d-116"><span id="vmUSBDeviceClass_HID"></span><span id="vmusbdeviceclass_hid"></span><span id="VMUSBDEVICECLASS_HID"></span>**vmUSBDeviceClass\_HID**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-117">Périphérique HID.</span><span class="sxs-lookup"><span data-stu-id="f897d-117">HID device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-118"><span id="vmUSBDeviceClass_Physical"></span><span id="vmusbdeviceclass_physical"></span><span id="VMUSBDEVICECLASS_PHYSICAL"></span>**vmUSBDeviceClass \_ physique**</span><span class="sxs-lookup"><span data-stu-id="f897d-118"><span id="vmUSBDeviceClass_Physical"></span><span id="vmusbdeviceclass_physical"></span><span id="VMUSBDEVICECLASS_PHYSICAL"></span>**vmUSBDeviceClass\_Physical**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-119">Appareil capteur physique.</span><span class="sxs-lookup"><span data-stu-id="f897d-119">Physical sensory device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-120"><span id="vmUSBDeviceClass_Image"></span><span id="vmusbdeviceclass_image"></span><span id="VMUSBDEVICECLASS_IMAGE"></span>**\_image vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="f897d-120"><span id="vmUSBDeviceClass_Image"></span><span id="vmusbdeviceclass_image"></span><span id="VMUSBDEVICECLASS_IMAGE"></span>**vmUSBDeviceClass\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-121">Périphérique d’analyse ou d’acquisition d’images.</span><span class="sxs-lookup"><span data-stu-id="f897d-121">Scanning or imaging device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-122"><span id="vmUSBDeviceClass_Printer"></span><span id="vmusbdeviceclass_printer"></span><span id="VMUSBDEVICECLASS_PRINTER"></span>**\_imprimante vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="f897d-122"><span id="vmUSBDeviceClass_Printer"></span><span id="vmusbdeviceclass_printer"></span><span id="VMUSBDEVICECLASS_PRINTER"></span>**vmUSBDeviceClass\_Printer**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-123">Périphérique d’impression.</span><span class="sxs-lookup"><span data-stu-id="f897d-123">Printer device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-124"><span id="vmUSBDeviceClass_MassStorage"></span><span id="vmusbdeviceclass_massstorage"></span><span id="VMUSBDEVICECLASS_MASSSTORAGE"></span>**vmUSBDeviceClass \_ MassStorage**</span><span class="sxs-lookup"><span data-stu-id="f897d-124"><span id="vmUSBDeviceClass_MassStorage"></span><span id="vmusbdeviceclass_massstorage"></span><span id="VMUSBDEVICECLASS_MASSSTORAGE"></span>**vmUSBDeviceClass\_MassStorage**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-125">Dispositif de stockage de masse.</span><span class="sxs-lookup"><span data-stu-id="f897d-125">Mass storage device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-126"><span id="vmUSBDeviceClass_Hub"></span><span id="vmusbdeviceclass_hub"></span><span id="VMUSBDEVICECLASS_HUB"></span>**\_Hub vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="f897d-126"><span id="vmUSBDeviceClass_Hub"></span><span id="vmusbdeviceclass_hub"></span><span id="VMUSBDEVICECLASS_HUB"></span>**vmUSBDeviceClass\_Hub**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-127">Périphérique Hub.</span><span class="sxs-lookup"><span data-stu-id="f897d-127">Hub device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-128"><span id="vmUSBDeviceClass_CDCData"></span><span id="vmusbdeviceclass_cdcdata"></span><span id="VMUSBDEVICECLASS_CDCDATA"></span>**vmUSBDeviceClass \_ CDCData**</span><span class="sxs-lookup"><span data-stu-id="f897d-128"><span id="vmUSBDeviceClass_CDCData"></span><span id="vmusbdeviceclass_cdcdata"></span><span id="VMUSBDEVICECLASS_CDCDATA"></span>**vmUSBDeviceClass\_CDCData**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-129">Appareil de données CDC.</span><span class="sxs-lookup"><span data-stu-id="f897d-129">CDC data device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-130"><span id="vmUSBDeviceClass_SmartCard"></span><span id="vmusbdeviceclass_smartcard"></span><span id="VMUSBDEVICECLASS_SMARTCARD"></span>**\_carte à puce vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="f897d-130"><span id="vmUSBDeviceClass_SmartCard"></span><span id="vmusbdeviceclass_smartcard"></span><span id="VMUSBDEVICECLASS_SMARTCARD"></span>**vmUSBDeviceClass\_SmartCard**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-131">Périphérique de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="f897d-131">Smart card device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-132"><span id="vmUSBDeviceClass_ContentSecurity"></span><span id="vmusbdeviceclass_contentsecurity"></span><span id="VMUSBDEVICECLASS_CONTENTSECURITY"></span>**vmUSBDeviceClass \_ contentsecurity**</span><span class="sxs-lookup"><span data-stu-id="f897d-132"><span id="vmUSBDeviceClass_ContentSecurity"></span><span id="vmusbdeviceclass_contentsecurity"></span><span id="VMUSBDEVICECLASS_CONTENTSECURITY"></span>**vmUSBDeviceClass\_ContentSecurity**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-133">Périphérique de sécurité du contenu.</span><span class="sxs-lookup"><span data-stu-id="f897d-133">Content security device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-134"><span id="vmUSBDeviceClass_Video"></span><span id="vmusbdeviceclass_video"></span><span id="VMUSBDEVICECLASS_VIDEO"></span>**\_vidéo vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="f897d-134"><span id="vmUSBDeviceClass_Video"></span><span id="vmusbdeviceclass_video"></span><span id="VMUSBDEVICECLASS_VIDEO"></span>**vmUSBDeviceClass\_Video**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-135">Périphérique vidéo.</span><span class="sxs-lookup"><span data-stu-id="f897d-135">Video device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-136"><span id="vmUSBDeviceClass_PersonalHealthcare"></span><span id="vmusbdeviceclass_personalhealthcare"></span><span id="VMUSBDEVICECLASS_PERSONALHEALTHCARE"></span>**vmUSBDeviceClass \_ PersonalHealthcare**</span><span class="sxs-lookup"><span data-stu-id="f897d-136"><span id="vmUSBDeviceClass_PersonalHealthcare"></span><span id="vmusbdeviceclass_personalhealthcare"></span><span id="VMUSBDEVICECLASS_PERSONALHEALTHCARE"></span>**vmUSBDeviceClass\_PersonalHealthcare**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-137">Appareil de soins de santé.</span><span class="sxs-lookup"><span data-stu-id="f897d-137">Health care device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-138"><span id="vmUSBDeviceClass_DiagnosticDevice"></span><span id="vmusbdeviceclass_diagnosticdevice"></span><span id="VMUSBDEVICECLASS_DIAGNOSTICDEVICE"></span>**vmUSBDeviceClass \_ DiagnosticDevice**</span><span class="sxs-lookup"><span data-stu-id="f897d-138"><span id="vmUSBDeviceClass_DiagnosticDevice"></span><span id="vmusbdeviceclass_diagnosticdevice"></span><span id="VMUSBDEVICECLASS_DIAGNOSTICDEVICE"></span>**vmUSBDeviceClass\_DiagnosticDevice**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-139">Périphérique de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="f897d-139">Diagnostic device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-140"><span id="vmUSBDeviceClass_WirelessController"></span><span id="vmusbdeviceclass_wirelesscontroller"></span><span id="VMUSBDEVICECLASS_WIRELESSCONTROLLER"></span>**vmUSBDeviceClass \_ WirelessController**</span><span class="sxs-lookup"><span data-stu-id="f897d-140"><span id="vmUSBDeviceClass_WirelessController"></span><span id="vmusbdeviceclass_wirelesscontroller"></span><span id="VMUSBDEVICECLASS_WIRELESSCONTROLLER"></span>**vmUSBDeviceClass\_WirelessController**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-141">Appareil sans fil.</span><span class="sxs-lookup"><span data-stu-id="f897d-141">Wireless device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-142"><span id="vmUSBDeviceClass_Miscellaneous"></span><span id="vmusbdeviceclass_miscellaneous"></span><span id="VMUSBDEVICECLASS_MISCELLANEOUS"></span>**vmUSBDeviceClass \_ divers**</span><span class="sxs-lookup"><span data-stu-id="f897d-142"><span id="vmUSBDeviceClass_Miscellaneous"></span><span id="vmusbdeviceclass_miscellaneous"></span><span id="VMUSBDEVICECLASS_MISCELLANEOUS"></span>**vmUSBDeviceClass\_Miscellaneous**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-143">Appareil divers.</span><span class="sxs-lookup"><span data-stu-id="f897d-143">Miscellaneous device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-144"><span id="vmUSBDeviceClass_ApplicationSpecific"></span><span id="vmusbdeviceclass_applicationspecific"></span><span id="VMUSBDEVICECLASS_APPLICATIONSPECIFIC"></span>**vmUSBDeviceClass \_ ApplicationSpecific**</span><span class="sxs-lookup"><span data-stu-id="f897d-144"><span id="vmUSBDeviceClass_ApplicationSpecific"></span><span id="vmusbdeviceclass_applicationspecific"></span><span id="VMUSBDEVICECLASS_APPLICATIONSPECIFIC"></span>**vmUSBDeviceClass\_ApplicationSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-145">Appareil spécifique à l’application.</span><span class="sxs-lookup"><span data-stu-id="f897d-145">Application-specific device.</span></span>

</dd> <dt>

<span data-ttu-id="f897d-146"><span id="vmUSBDeviceClass_VendorSpecific"></span><span id="vmusbdeviceclass_vendorspecific"></span><span id="VMUSBDEVICECLASS_VENDORSPECIFIC"></span>**vmUSBDeviceClass \_ VendorSpecific**</span><span class="sxs-lookup"><span data-stu-id="f897d-146"><span id="vmUSBDeviceClass_VendorSpecific"></span><span id="vmusbdeviceclass_vendorspecific"></span><span id="VMUSBDEVICECLASS_VENDORSPECIFIC"></span>**vmUSBDeviceClass\_VendorSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="f897d-147">Appareil spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f897d-147">Vendor-specific device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f897d-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f897d-148">Requirements</span></span>



| <span data-ttu-id="f897d-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f897d-149">Requirement</span></span> | <span data-ttu-id="f897d-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="f897d-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f897d-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f897d-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f897d-152">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f897d-152">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f897d-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f897d-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f897d-154">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f897d-154">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f897d-155">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f897d-155">End of client support</span></span><br/>    | <span data-ttu-id="f897d-156">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f897d-156">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f897d-157">Produit</span><span class="sxs-lookup"><span data-stu-id="f897d-157">Product</span></span><br/>                  | <span data-ttu-id="f897d-158">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f897d-158">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f897d-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="f897d-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="f897d-160"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f897d-160"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f897d-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f897d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f897d-162">**IVMUSBDevice ::D eviceClass**</span><span class="sxs-lookup"><span data-stu-id="f897d-162">**IVMUSBDevice::DeviceClass**</span></span>](ivmusbdevice-deviceclass.md)
</dt> </dl>

 

