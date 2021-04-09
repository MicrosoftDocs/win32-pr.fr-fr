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
ms.openlocfilehash: e813538cfcb995949cbe1fb8ec6a3b0d7772061c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740597"
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

Chemin d’accès (emplacement) à la tâche dans un dossier. Le dossier de tâches racine est spécifié avec une barre oblique inverse ( \) . Un exemple de chemin d’accès à un dossier de tâches, sous le dossier racine de la tâche, est \\ MyTaskFolder. Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. ' les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.

## <a name="error-codes"></a>Codes d’erreur

Tâche à l’emplacement spécifié. La tâche est un objet [**RegisteredTask**](registeredtask.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





