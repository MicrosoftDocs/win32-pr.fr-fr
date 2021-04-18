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
ms.openlocfilehash: e0f98318ba8332e4c3bb0e7fee6b702a7ed50533
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509335"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> </dl>

 

 





