---
title: ComHandlerAction. ClassId, propriété
description: Pour les scripts, obtient ou définit l’identificateur de la classe de gestionnaire.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- Propriété ClassId Planificateur de tâches
- ClassId, propriété Planificateur de tâches, objet ComHandlerAction
- Objet ComHandlerAction Planificateur de tâches, propriété ClassId
topic_type:
- apiref
api_name:
- ComHandlerAction.ClassId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72338d4fe15936fcfe8f158098a798c4a3630cbd0587f46dc2f9346405477a59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100459"
---
# <a name="comhandleractionclassid-property"></a>ComHandlerAction. ClassId, propriété

Pour les scripts, obtient ou définit l’identificateur de la classe de gestionnaire.

## <a name="syntax"></a>Syntaxe


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur de la classe qui définit le gestionnaire à déclencher.

## <a name="remarks"></a>Remarques

Lors de la lecture ou de l’écriture de données XML, la classe d’un gestionnaire COM est spécifiée dans l’élément [**ClassID**](taskschedulerschema-classid-comhandlertype-element.md) du schéma planificateur de tâches.

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

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 





