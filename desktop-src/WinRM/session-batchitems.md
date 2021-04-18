---
title: Session.Batpropriété chItems (WSManDisp. h)
description: Définit et obtient le nombre d’éléments dans chaque lot d’énumération.
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la propriété BatchItems
- Propriété BatchItems Windows Remote Management, objet session
- Windows Remote Management d’objet de session, propriété BatchItems
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb668b80a2fea8ec5c8683a7a85a20cfbb217a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512192"
---
# <a name="sessionbatchitems-property"></a>Session.Batpropriété chItems

Définit et obtient le nombre d’éléments dans chaque lot d’énumération. Cette valeur ne peut pas être modifiée pendant une énumération. Le fournisseur de ressources peut définir une limite.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Session.BatchItems As long
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie le nombre maximal d’éléments retournés pour chaque appel réseau sous-jacent au service. Valeur par défaut : 20.

## <a name="remarks"></a>Notes

Il s’agit d’une fonctionnalité d’optimisation qui contrôle la fréquence des appels réseau entre le client et le serveur. Actuellement, elle est utilisée uniquement pour les énumérations. Pour plus d’informations sur l’énumération des ressources, consultez [**énumérer**](session-enumerate.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**session**](session.md)
</dt> <dt>

[**Énumérer**](session-enumerate.md)
</dt> <dt>

[**Enumerator. ReadItem**](enumerator-readitem.md)
</dt> </dl>

 

 





