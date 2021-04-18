---
title: Méthode IVMVirtualMachine DetachUSBDevice (VPCCOMInterfaces. h)
description: Libère un périphérique USB d’un ordinateur virtuel.
ms.assetid: ae2b70b1-7bf3-4a84-9f05-4e91de93fa73
keywords:
- Méthode DetachUSBDevice Virtual PC
- Méthode DetachUSBDevice Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode DetachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DetachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f5a858c25822e9e9ba1a11686003b326133a59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106540779"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a>IVMVirtualMachine ::D méthode etachUSBDevice

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Libère un périphérique USB d’un ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*inUSBDevice* \[ dans\]
</dt> <dd>

Pointeur [**IVMUSBDevice**](ivmusbdevice.md) qui représente le périphérique USB à détacher de la machine virtuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                          | Description                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                | L'opération a réussi.<br/>       |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                  | Le paramètre a la **valeur null**.<br/>          |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt> </dl>     | L’ordinateur virtuel n’est pas en cours d’exécution.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ \_ \_ \_ Échec du détachement d’E**</dt> /r USB <dt>0xA00400927</dt> </dl> | L’opération de détachement a échoué.<br/>        |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>          | Une erreur inattendue s’est produite.<br/>   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

