---
title: Méthode IVMVirtualMachineEvents OnRequestShutdown (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant qu’une demande d’arrêt a été effectuée.
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- Méthode OnRequestShutdown Virtual PC
- Méthode OnRequestShutdown Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, méthode OnRequestShutdown
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnRequestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 929c9a293e760a12ace62766cbd7a0c016980fc2399cdde494402a272d90fe0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123169"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a>IVMVirtualMachineEvents :: OnRequestShutdown, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Reçoit une notification indiquant qu’une demande d’arrêt a été effectuée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode est appelée chaque fois que la session de l’ordinateur virtuel va être arrêtée. Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l’événement **vmVirtualMachineEvent \_ RequestShutdown** provenant de [**IVMVirtualMachine**](ivmvirtualmachine.md).

Cette notification d’événement est envoyée uniquement lorsque la session machines virtuelles est sur le paragraphe d’être arrêtée. Les routines d’arrêt du système d’exploitation, telles que [**IVMGuestOS :: Shutdown**](ivmguestos-shutdown.md), ne déclenchent pas cet événement directement, sauf si elles tentent également d’effectuer une mise hors tension logicielle du matériel virtuel.

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

 

