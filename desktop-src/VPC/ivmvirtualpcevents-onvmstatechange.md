---
title: Méthode IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que l’état d’une machine virtuelle a changé. | Méthode IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- Méthode OnVMStateChange Virtual PC
- Méthode OnVMStateChange Virtual PC, interface IVMVirtualPCEvents
- IVMVirtualPCEvents interface Virtual PC, méthode OnVMStateChange
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnVMStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63516e80ce4f3b830229fdb4cd574e95378c0569a4855a73c1c528af2ec8b48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032979"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a>IVMVirtualPCEvents :: OnVMStateChange, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Reçoit une notification indiquant que l’état d’une machine virtuelle a changé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*virtualMachineConfig* \[ dans\]
</dt> <dd>

Nom de la machine virtuelle.

</dd> <dt>

*virtualMachineState* \[ dans\]
</dt> <dd>

Nouvel état de la machine virtuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l’événement **vmVirtualPCEvent \_ VMStateChanged** provenant de [**IVMVirtualPC**](ivmvirtualpc.md). Pour surveiller un ordinateur virtuel spécifique, utilisez la méthode [**IVMVirtualMachineEvents :: OnStateChange**](ivmvirtualmachineevents-onstatechange.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents est défini comme efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

