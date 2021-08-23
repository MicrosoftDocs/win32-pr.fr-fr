---
title: Méthode IVMVirtualMachineEvents OnAdditionsAvailable (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant que les composants d’intégration sont disponibles sur une machine virtuelle.
ms.assetid: c940104b-4d34-47c2-bf48-9024a7f86c46
keywords:
- Méthode OnAdditionsAvailable Virtual PC
- Méthode OnAdditionsAvailable Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, méthode OnAdditionsAvailable
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsAvailable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81657563a921ca8a9aa7ef511183a56aa2d7a599e69232fcc186d7d911cb65bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056748"
---
# <a name="ivmvirtualmachineeventsonadditionsavailable-method"></a>IVMVirtualMachineEvents :: OnAdditionsAvailable, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Reçoit une notification indiquant que les composants d’intégration sont disponibles sur une machine virtuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnAdditionsAvailable();
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

 

