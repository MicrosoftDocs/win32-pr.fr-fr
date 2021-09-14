---
title: TaskSettings. Hidden, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche ne sera pas visible dans l’interface utilisateur.
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- Planificateur de tâches de propriétés masquées
- Propriété masquée Planificateur de tâches, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété masquée
topic_type:
- apiref
api_name:
- TaskSettings.Hidden
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057a3d920ba70260d23ad13a5888072ab5b07767
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920191"
---
# <a name="tasksettingshidden-property"></a>TaskSettings. Hidden, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche ne sera pas visible dans l’interface utilisateur. Toutefois, les administrateurs peuvent remplacer ce paramètre à l’aide d’un « commutateur maître » qui rend toutes les tâches visibles dans l’interface utilisateur.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la valeur est **true**, la valeur indique que la tâche ne sera pas visible dans l’interface utilisateur. Si la **valeur est false**, la tâche est visible dans l’interface utilisateur. La valeur par défaut est **False**.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Spécifications



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

 

 





