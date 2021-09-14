---
title: Propriété principal. GroupId
description: Pour les scripts, obtient ou définit l’identificateur du groupe d’utilisateurs requis pour exécuter les tâches associées au principal.
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- Propriété GroupId Planificateur de tâches
- Propriété GroupId Planificateur de tâches, objet principal
- Objet principal Planificateur de tâches, propriété GroupId
topic_type:
- apiref
api_name:
- Principal.GroupId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5acd17d32b0123723fe53f91e390c37f42d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122986"
---
# <a name="principalgroupid-property"></a>Propriété principal. GroupId

Pour les scripts, obtient ou définit l’identificateur du groupe d’utilisateurs requis pour exécuter les tâches associées au principal.

## <a name="syntax"></a>Syntaxe


```VB
Principal.GroupId As String
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur du groupe d’utilisateurs associé à ce principal.

## <a name="remarks"></a>Notes

Ne définissez pas cette propriété si un identificateur d’utilisateur est spécifié dans la propriété [**userid**](principal-userid.md) .

Lors de la lecture ou de l’écriture de données XML pour une tâche, l’identificateur de groupe pour un principal est spécifié dans l’élément [**GroupID**](taskschedulerschema-groupid-principaltype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**UserId**](principal-userid.md)
</dt> <dt>

[**Principal**](principal.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





