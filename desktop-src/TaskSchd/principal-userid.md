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
ms.openlocfilehash: 9501184f3316e464aa26f42d51e0b4c27eccaeb72d447faa91edaa33b0b4774c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060027"
---
# <a name="principaluserid-property"></a>Propriété principal. UserId

Pour les scripts, obtient ou définit l’identificateur de l’utilisateur qui est requis pour exécuter les tâches associées au principal.

## <a name="syntax"></a>Syntaxe


```VB
Principal.UserId As String
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur d’utilisateur requis pour exécuter la tâche.

## <a name="remarks"></a>Remarques

Ne définissez pas cette propriété si un identificateur de groupe est spécifié dans la propriété [**GroupID**](principal-groupid.md) .

Lors de la lecture ou de l’écriture de données XML pour une tâche, l’identificateur d’utilisateur du principal est spécifié à l’aide de l’élément [**userid**](taskschedulerschema-userid-principaltype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[**Principal**](principal.md)
</dt> <dt>

[**Principal. GroupId**](principal-groupid.md)
</dt> </dl>

 

 





