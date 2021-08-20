---
title: Méthode IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que l’état d’une machine virtuelle a changé. | Méthode IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces. h)
ms.assetid: 1737bb5e-078d-4ebe-9558-de083aae1baa
keywords:
- Méthode OnStateChange Virtual PC
- Méthode OnStateChange Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, méthode OnStateChange
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf966d2439f3095051331b5412bc92cca9ba76e6f98c9777402ba449f2e7f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122699"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a>IVMVirtualMachineEvents :: OnStateChange, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Reçoit une notification indiquant que l’état d’une machine virtuelle a changé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*virtualMachineState* \[ dans\]
</dt> <dd>

Nouvel état de la machine virtuelle. Pour obtenir la liste des valeurs, consultez [**VMVMState**](vmvmstate.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode est appelée lorsque l’état de cet ordinateur virtuel change. Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l' \_ événement vmVirtualMachineEvent StateChanged provenant de [**IVMVirtualMachine**](ivmvirtualmachine.md).

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

 

