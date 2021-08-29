---
title: Méthode IVMVirtualMachineEvents OnGuestShutdown (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que le système d’exploitation invité s’arrête.
ms.assetid: a70c746a-f1ce-4f93-b41b-b03dc83f3da2
keywords:
- Méthode OnGuestShutdown Virtual PC
- Méthode OnGuestShutdown Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, méthode OnGuestShutdown
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4da02164e22321842d09a29c4a8a286edfe548108afd927b3127886a98f6e05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056567"
---
# <a name="ivmvirtualmachineeventsonguestshutdown-method"></a>IVMVirtualMachineEvents :: OnGuestShutdown, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Reçoit une notification indiquant que le système d’exploitation invité s’arrête.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnGuestShutdown();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents est défini comme 9d84f560-bb67-4961-BD12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

