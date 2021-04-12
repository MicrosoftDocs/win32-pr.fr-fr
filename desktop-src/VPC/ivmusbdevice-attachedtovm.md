---
title: IVMUSBDevice AttachedToVM, propriété (VPCCOMInterfaces. h)
description: Récupère le nom de l’ordinateur virtuel auquel le périphérique USB est attaché.
ms.assetid: 214ed891-1fca-4311-945a-0ce3d05d604e
keywords:
- AttachedToVM propriété Virtual PC
- AttachedToVM, propriété Virtual PC, IVMUSBDevice, interface
- IVMUSBDevice interface Virtual PC, propriété AttachedToVM
topic_type:
- apiref
api_name:
- IVMUSBDevice.AttachedToVM
- IVMUSBDevice.get_AttachedToVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c64e265cba81858bc887cbf595426bffd1b604aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032928"
---
# <a name="ivmusbdeviceattachedtovm-property"></a>IVMUSBDevice :: AttachedToVM, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le nom de l’ordinateur virtuel auquel le périphérique USB est attaché.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_AttachedToVM(
  [out, retval] BSTR *ConfigName
);
```



## <a name="property-value"></a>Valeur de la propriété

Nom de la machine virtuelle.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                           | Signification                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                              | L’appareil est attaché à la machine virtuelle et son nom est retourné.<br/> |
| <dl> <dt>S \_ FALSe</dt> <dt>1</dt> </dl>                           | L’appareil est attaché à l’ordinateur hôte.<br/>                         |
| <dl> <dt>Ordinateur virtuel \_ 0xA00400929 \_ d' \_ \_ ordinateur virtuel externe USB</dt> <dt></dt> </dl> | L’appareil est attaché à une machine virtuelle dans une autre session utilisateur.<br/>     |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                | Le paramètre a la **valeur null**.<br/>                                  |



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

 

