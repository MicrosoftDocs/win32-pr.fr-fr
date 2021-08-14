---
title: TaskFolder. GetTask, propriété
description: Pour les scripts, obtient une tâche à un emplacement spécifié dans un dossier.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Planificateur de tâches de la propriété GetTask
- Planificateur de tâches de la propriété GetTask, objet TaskFolder
- Planificateur de tâches objet TaskFolder, propriété GetTask
topic_type:
- apiref
api_name:
- TaskFolder.GetTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8369c09ad62329fa583bfba1cf718a3543c565f3e3d41f1d20f88339e37c44ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253419"
---
# <a name="taskfoldergettask-property"></a>TaskFolder. GetTask, propriété

Pour les scripts, obtient une tâche à un emplacement spécifié dans un dossier.

## <a name="syntax"></a>Syntaxe


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a>Valeur de la propriété

Chemin d’accès (emplacement) à la tâche dans un dossier. Le dossier de tâches racine est spécifié avec une barre oblique inverse ( \\ ). Un exemple de chemin d’accès à un dossier de tâches, sous le dossier racine de la tâche, est \\ MyTaskFolder. Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. ' les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.

## <a name="error-codes"></a>Codes d’erreur

Tâche à l’emplacement spécifié. La tâche est un objet [**RegisteredTask**](registeredtask.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





