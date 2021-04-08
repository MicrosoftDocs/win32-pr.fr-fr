---
title: Propriété ID IVMTask (VPCCOMInterfaces. h)
description: Récupère un identificateur unique pour cette tâche.
ms.assetid: 56a63b94-139b-4445-aef6-1b988e548b4b
keywords:
- Propriété d’ID Virtual PC
- Propriété d’ID Virtual PC, interface IVMTask
- IVMTask interface Virtual PC, propriété ID
topic_type:
- apiref
api_name:
- IVMTask.ID
- IVMTask.get_ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821650fcec725a43d86e539bd7f6cc9e7a6e2677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844145"
---
# <a name="ivmtaskid-property"></a>IVMTask :: ID, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère un identificateur unique pour cette tâche.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_ID(
  [out, retval] long *ID
);
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur unique.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>     |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | La valeur du paramètre est **null**.<br/>  |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask est défini en tant que ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

