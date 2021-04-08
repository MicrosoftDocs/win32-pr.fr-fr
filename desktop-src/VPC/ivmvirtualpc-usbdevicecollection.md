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
# <a name="ivmvirtualpcusbdevicecollection-property"></a>IVMVirtualPC :: USBDeviceCollection, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère une collection énumérable de tous les périphériques USB connectés à l’hôte.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_USBDeviceCollection(
  [out, retval] IVMUSBDeviceCollection **usbDeviceCollection
);
```



## <a name="property-value"></a>Valeur de la propriété

Référence à un pointeur [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md) qui représente une collection d’objets [**IVMUSBDevice**](ivmusbdevice.md) .

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                                | Signification                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                   | L'opération a réussi.<br/>                                                        |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                                     | Le paramètre a la **valeur null**.<br/>                                                           |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                             | Une erreur inattendue s’est produite.<br/>                                                    |
| <dl> <dt>Ordinateur virtuel \_ Échec de l' \_ énumération E USB- \_ nombre d' \_ \_ \_ appareils</dt> <dt>0xA0040930</dt> </dl> | Plus de 16 périphériques USB sont connectés à l’ordinateur hôte.<br/>                                  |
| <dl> <dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt> </dl>      | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

