---
title: TaskFolder. GetFolder, propriété
description: Pour les scripts, obtient un dossier qui contient des tâches à un emplacement spécifié.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- Planificateur de tâches de propriété GetFolder
- Propriété GetFolder Planificateur de tâches, objet TaskFolder
- Objet TaskFolder Planificateur de tâches, GetFolder, propriété
topic_type:
- apiref
api_name:
- TaskFolder.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65b3f50cc5b8ab75bb041a61b36ad66bb35891
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387028"
---
# <a name="taskfoldergetfolder-property"></a>TaskFolder. GetFolder, propriété

Pour les scripts, obtient un dossier qui contient des tâches à un emplacement spécifié.

## <a name="syntax"></a>Syntaxe


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a>Valeur de la propriété

Chemin d’accès (emplacement) au dossier. N’utilisez pas de barre oblique inverse à la suite du nom du dernier dossier dans le chemin d’accès. Le dossier de tâches racine est spécifié avec une barre oblique inverse ( \\ ). Un exemple de chemin d’accès à un dossier de tâches, sous le dossier racine de la tâche, est \\ MyTaskFolder. Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. ' les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.

## <a name="error-codes"></a>Codes d’erreur

Dossier à l’emplacement spécifié. Le dossier est un objet [**TaskFolder**](taskfolder.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





