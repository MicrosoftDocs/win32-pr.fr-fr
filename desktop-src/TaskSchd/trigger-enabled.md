---
title: Déclencheur. Enabled, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.
ms.assetid: 8fb5a0cc-ddd4-430d-9593-95a4cb311f18
keywords:
- Planificateur de tâches de la propriété Enabled
- Propriété Enabled Planificateur de tâches, objet Trigger
- Objet Trigger Planificateur de tâches, propriété Enabled
topic_type:
- apiref
api_name:
- Trigger.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b9fe5439576322807abea6e10089460eaed4440496ed6a9e0f989dd44bc7e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099699"
---
# <a name="triggerenabled-property"></a>Déclencheur. Enabled, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.

## <a name="syntax"></a>Syntaxe


```VB
Trigger.Enabled As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

True si le déclencheur est activé ; Sinon, false. La valeur par défaut est true.

## <a name="remarks"></a>Remarques

Lors de la lecture ou de l’écriture de données XML pour une tâche, la propriété Enabled est spécifiée à l’aide de l’élément [**Enabled**](taskschedulerschema-enabled-triggerbasetype-element.md) du schéma planificateur de tâches.

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
</dt> </dl>

 

 





