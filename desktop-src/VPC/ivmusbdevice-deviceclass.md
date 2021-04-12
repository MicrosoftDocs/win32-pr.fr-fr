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
# <a name="ivmusbdevicedeviceclass-property"></a>IVMUSBDevice ::D propriété eviceClass

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère la classe de périphérique du périphérique USB.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DeviceClass(
  [out, retval] VMUSBDeviceClassEnum *deviceClass
);
```



## <a name="property-value"></a>Valeur de la propriété

Classe de l’appareil. Pour obtenir la liste des valeurs, consultez [**VMUSBDeviceClassEnum**](vmusbdeviceclassenum.md).

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                            | Signification                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>               | La commande s'est correctement terminée.<br/> |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl> | Le paramètre a la **valeur null**.<br/>         |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice est défini en tant que 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

