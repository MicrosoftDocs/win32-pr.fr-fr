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
# <a name="ivmusbdevice-interface"></a>Interface IVMUSBDevice

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit l’interface pour un périphérique USB attaché à l’hôte. Vous pouvez attacher un périphérique USB à un ordinateur virtuel pour utiliser l’appareil à l’intérieur de la machine virtuelle.

## <a name="members"></a>Membres

L’interface **IVMUSBDevice** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMUSBDevice** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IVMUSBDevice** possède les propriétés suivantes.



| Propriété                                                                 | Type d’accès          | Description                                                                     |
|:-------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [**AttachedToVM**](ivmusbdevice-attachedtovm.md)<br/>             | Lecture seule<br/> | Nom de la machine virtuelle à laquelle le périphérique USB est attaché.<br/> |
| [**DeviceClass**](ivmusbdevice-deviceclass.md)<br/>               | Lecture seule<br/> | Classe de périphérique du périphérique USB.<br/>                                  |
| [**DeviceString**](ivmusbdevice-devicestring.md)<br/>             | Lecture seule<br/> | Nom du périphérique USB.<br/>                                          |
| [**HubID**](ivmusbdevice-hubid.md)<br/>                           | Lecture seule<br/> | Identificateur du concentrateur sur lequel l’appareil est connecté.<br/>          |
| [**ManufacturerString**](ivmusbdevice-manufacturerstring.md)<br/> | Lecture seule<br/> | Nom du fabricant du périphérique USB.<br/>                             |
| [**Port**](ivmusbdevice-port.md)<br/>                             | Lecture seule<br/> | Identificateur du port sur lequel l’appareil est connecté.<br/>         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice est défini en tant que 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



 

