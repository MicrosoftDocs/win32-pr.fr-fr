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
ms.openlocfilehash: 1daf5df827bd9d890ede26242957adb2da8a025e8b1d272254e145b12f5aee91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752538"
---
# <a name="ivmusbdevicecollection-interface"></a>Interface IVMUSBDeviceCollection

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit la collection des périphériques USB attachés au système hôte. Pour obtenir un objet **IVMUSBDeviceCollection** , utilisez la propriété [**IVMVirtualPC :: USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md) .

## <a name="members"></a>Membres

L’interface **IVMUSBDeviceCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMUSBDeviceCollection** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IVMUSBDeviceCollection** possède les propriétés suivantes.



| Propriété                                                        | Type d’accès          | Description                                                                         |
|:----------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmusbdevicecollection--newenum.md)<br/> | Lecture seule<br/> | Énumérateur de la collection.<br/>                                        |
| [**Count**](ivmusbdevicecollection-count.md)<br/>        | Lecture seule<br/> | Nombre de périphériques USB dans ce regroupement.<br/>                            |
| [**Élément**](ivmusbdevicecollection-item.md)<br/>          | Lecture seule<br/> | Objet périphérique USB qui correspond à l’index spécifié (basé sur 1).<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDeviceCollection est défini en tant que 4FBCD6A5-F53C-4D1C-9F4D-E90ABB8B3749<br/>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> <dt>

[**IVMVirtualPC::USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)
</dt> </dl>

 

