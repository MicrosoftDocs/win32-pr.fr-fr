---
title: Propriété d’erreur IVMTask (VPCCOMInterfaces. h)
description: Récupère l’erreur enregistrée pour cette tâche.
ms.assetid: 9023e24b-679b-43e4-8db4-b8510a582382
keywords:
- Propriété d’erreur Virtual PC
- Propriété d’erreur Virtual PC, interface IVMTask
- IVMTask interface Virtual PC, propriété Error
topic_type:
- apiref
api_name:
- IVMTask.Error
- IVMTask.get_Error
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d75c4748678fb2ba500ae7a772afe9fb4a8147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510146"
---
# <a name="ivmtaskerror-property"></a>IVMTask :: Error, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère l’erreur enregistrée pour cette tâche.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Error(
  [out, retval] long *outError
);
```



## <a name="property-value"></a>Valeur de la propriété

Erreur enregistrée.

## <a name="error-codes"></a>Codes d’erreur

Les instances de [**IVMTask**](ivmtask.md) retournées par d’autres interfaces peuvent retourner des valeurs supplémentaires. Pour plus d’informations, consultez la documentation des méthodes qui retournent une instance **IVMTask** .



| Nom/valeur                                                                                                                                                                        | Signification                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                           | L'opération a réussi.<br/>                              |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                             | La valeur du paramètre est **null**.<br/>                           |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                     | Une erreur inattendue s’est produite.<br/>                          |
| <dl> <dt>Ordinateur virtuel \_ E \_ VMVIRTUALPC \_ plus ancienne \_ version</dt> <dt>0xA0040952</dt> </dl>     | Virtual PC 2007 et Windows Virtual PC sont tous deux installés.<br/> |
| <dl> <dt>Ordinateur virtuel \_ 0xA0040953 d' \_ autres \_ \_ logiciels de virtualisation</dt> <dt></dt> </dl> | D’autres logiciels de virtualisation sont installés.<br/>                |



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

 

