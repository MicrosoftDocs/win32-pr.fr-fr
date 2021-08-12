---
title: IVMTask méthode Cancel (VPCCOMInterfaces. h)
description: Annule la tâche.
ms.assetid: 29107942-334c-452a-b787-6e0cb7380f90
keywords:
- Annuler la méthode Virtual PC
- Méthode Cancel Virtual PC, interface IVMTask
- IVMTask interface Virtual PC, méthode Cancel
topic_type:
- apiref
api_name:
- IVMTask.Cancel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0580adb49306397460bd99b0135a13956d01b0a839b72e0ae8ae19f00f7c929e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593142"
---
# <a name="ivmtaskcancel-method"></a>IVMTask :: Cancel, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Annule la tâche.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                 | Description                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>     |
| <dl> <dt>**E \_ ÉCHEC**</dt> <dt>0x80004005</dt> </dl>            | La tâche ne peut pas être annulée.<br/>      |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask est défini en tant que ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

