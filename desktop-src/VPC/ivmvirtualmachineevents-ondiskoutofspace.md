---
title: Méthode IVMVirtualMachineEvents OnDiskOutOfSpace (VPCCOMInterfaces. h)
description: Reçoit une notification indiquant qu’un disque requis pour une machine virtuelle ne dispose pas de suffisamment d’espace libre.
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- Méthode OnDiskOutOfSpace Virtual PC
- Méthode OnDiskOutOfSpace Virtual PC, interface IVMVirtualMachineEvents
- IVMVirtualMachineEvents interface Virtual PC, méthode OnDiskOutOfSpace
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnDiskOutOfSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac2d5f45068dc8cd7341d0a599b2da4e5c7655a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843034"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a>IVMVirtualMachineEvents :: OnDiskOutOfSpace, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Reçoit une notification indiquant qu’un disque requis pour un ordinateur virtuel ne dispose pas de suffisamment d’espace libre. Si l’espace libre descend en dessous de 100 Mo, cet événement est reçu en tant qu’avertissement et si l’espace libre descend en dessous de 20 Mo, cet événement est de nouveau reçu en tant qu’erreur et la machine virtuelle est suspendue.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*criticallyLow* \[ dans\]
</dt> <dd>

Affectez la valeur **Variant \_ true** si le disque dispose de moins de 20 Mo de libre et la **\_ valeur false** si l’espace libre est supérieur à 20 Mo mais inférieur à 100 Mo.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents est défini comme 9d84f560-bb67-4961-BD12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

