---
title: Propriété principal. UserId
description: Pour les scripts, obtient ou définit l’identificateur de l’utilisateur qui est requis pour exécuter les tâches associées au principal.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- UserId, propriété Planificateur de tâches
- UserId, propriété Planificateur de tâches, objet principal
- Objet principal Planificateur de tâches, propriété UserId
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6fce7fcfdf235ba8a83f262161c2e0f2afc71c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104356"
---
# <a name="principaluserid-property"></a>Propriété principal. UserId

Pour les scripts, obtient ou définit l’identificateur de l’utilisateur qui est requis pour exécuter les tâches associées au principal.

## <a name="syntax"></a>Syntaxe


```VB
Principal.UserId As String
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur d’utilisateur requis pour exécuter la tâche.

## <a name="remarks"></a>Notes

Ne définissez pas cette propriété si un identificateur de groupe est spécifié dans la propriété [**GroupID**](principal-groupid.md) .

Lors de la lecture ou de l’écriture de données XML pour une tâche, l’identificateur d’utilisateur du principal est spécifié à l’aide de l’élément [**userid**](taskschedulerschema-userid-principaltype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[**Directeur**](principal.md)
</dt> <dt>

[**Principal. GroupId**](principal-groupid.md)
</dt> </dl>

 

 





