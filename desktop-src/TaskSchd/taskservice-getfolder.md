---
title: TaskService. GetFolder, méthode
description: Pour les scripts, obtient un dossier de tâches inscrites.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- Méthode GetFolder Planificateur de tâches
- Méthode GetFolder Planificateur de tâches, objet TaskService
- Objet TaskService Planificateur de tâches, méthode GetFolder
topic_type:
- apiref
api_name:
- TaskService.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74504e9cad124f8cbc9ec23e896ba4dec7d7f50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510368"
---
# <a name="taskservicegetfolder-method"></a>TaskService. GetFolder, méthode

Pour les scripts, obtient un dossier de tâches inscrites.

## <a name="syntax"></a>Syntaxe


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*chemin d’accès* \[ dans\]
</dt> <dd>

Chemin d’accès au dossier à récupérer. N’utilisez pas de barre oblique inverse à la suite du nom du dernier dossier dans le chemin d’accès. Le dossier de tâches racine est spécifié avec une barre oblique inverse ( \) . Un exemple de chemin d’accès à un dossier de tâches, sous le dossier racine de la tâche, est \\ MyTaskFolder. Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. ' les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Objet [**TaskFolder**](taskfolder.md) pour le dossier demandé.

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
</dt> </dl>

 

 





