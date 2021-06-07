---
title: TaskFolder. CreateFolder, méthode
description: Pour les scripts, crée un dossier pour les tâches associées.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- CreateFolder, méthode Planificateur de tâches
- CreateFolder, méthode Planificateur de tâches, objet TaskFolder
- Objet TaskFolder Planificateur de tâches, méthode CreateFolder
topic_type:
- apiref
api_name:
- TaskFolder.CreateFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a873ef59ea9d099a7a739e5238c722f4b908fd
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387077"
---
# <a name="taskfoldercreatefolder-method"></a>TaskFolder. CreateFolder, méthode

Pour les scripts, crée un dossier pour les tâches associées.

## <a name="syntax"></a>Syntaxe


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NomDossier* \[ dans\]
</dt> <dd>

Nom utilisé pour identifier le dossier. Si « NomDossier \\ sous \\ SubFolder2 » est spécifié, la totalité de l’arborescence de dossiers est créée si les dossiers n’existent pas. Ce paramètre peut être un chemin d’accès relatif à l’instance [**TaskFolder**](taskfolder.md) actuelle. Le dossier de tâches racine est spécifié avec une barre oblique inverse ( \\ ). Un exemple de chemin d’accès à un dossier de tâches, sous le dossier racine de la tâche, est \\ MyTaskFolder. Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. ' les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.

</dd> <dt>

*langage SDDL* \[ dans\]
</dt> <dd>

Descripteur de sécurité associé au dossier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Objet [**TaskFolder**](taskfolder.md) qui représente le nouveau sous-dossier.

## <a name="requirements"></a>Spécifications



| Condition requise | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





