---
title: Propriété Principal.Id
description: Pour les scripts, obtient ou définit l’identificateur du principal.
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- Propriété ID Planificateur de tâches
- ID de propriété Planificateur de tâches, objet principal
- Planificateur de tâches de l’objet principal, propriété ID
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122982"
---
# <a name="principalid-property"></a>Propriété Principal.Id

Pour les scripts, obtient ou définit l’identificateur du principal.

## <a name="syntax"></a>Syntaxe


```VB
Principal.Id As String
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur du principal.

## <a name="remarks"></a>Notes

Cet identificateur est également utilisé lors de la spécification de la propriété [**ActionCollection. Context**](actioncollection-context.md) .

Lors de la lecture ou de l’écriture de données XML pour une tâche, l’identificateur de l’entité de sécurité est spécifié dans l’attribut ID de l’élément [**principal**](taskschedulerschema-principal-principaltype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ActionCollection. Context**](actioncollection-context.md)
</dt> <dt>

[**Principal**](principal.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





