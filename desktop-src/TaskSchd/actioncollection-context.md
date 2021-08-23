---
title: ActionCollection. Context, propriété
description: Pour les scripts, obtient ou définit l’identificateur du principal pour la tâche.
ms.assetid: 5d8ac31c-ce07-4801-a04e-e12e996b88c6
keywords:
- Planificateur de tâches de la propriété de contexte
- Planificateur de tâches de propriété de contexte, objet ActionCollection
- Planificateur de tâches objet ActionCollection, propriété de contexte
topic_type:
- apiref
api_name:
- ActionCollection.Context
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff495e4ef2742a6a05570308f2976c014026941d290d44c39bdd087ce3e13a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772749"
---
# <a name="actioncollectioncontext-property"></a>ActionCollection. Context, propriété

Pour les scripts, obtient ou définit l’identificateur du principal pour la tâche.

## <a name="syntax"></a>Syntaxe


```VB
ActionCollection.Context As String
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur du principal de la tâche. L’identificateur spécifié ici doit correspondre à l’identificateur spécifié dans la propriété ID de l’interface IPrincipal qui définit le principal.

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

[**ActionCollection**](actioncollection.md)
</dt> </dl>

 

 





