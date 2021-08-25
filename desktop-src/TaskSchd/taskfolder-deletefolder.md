---
title: Méthode TaskFolder. DeleteFolder
description: Pour les scripts, supprime un sous-dossier du dossier parent.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Planificateur de tâches de la méthode DeleteFolder
- Méthode DeleteFolder Planificateur de tâches, objet TaskFolder
- Planificateur de tâches objet TaskFolder, méthode DeleteFolder
topic_type:
- apiref
api_name:
- TaskFolder.DeleteFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73dfe168b599de6e09d5437d0be4ec7a851d246f9fcbce0f79f662b62c56212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974899"
---
# <a name="taskfolderdeletefolder-method"></a>Méthode TaskFolder. DeleteFolder

Pour les scripts, supprime un sous-dossier du dossier parent.

## <a name="syntax"></a>Syntaxe


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NomDossier* \[ dans\]
</dt> <dd>

Nom du sous-dossier à supprimer. Le dossier de tâches racine est spécifié avec une barre oblique inverse ( \\ ). Ce paramètre peut être un chemin d’accès relatif au dossier que vous souhaitez supprimer. Un exemple de chemin d’accès à un dossier de tâches, sous le dossier racine de la tâche, est \\ MyTaskFolder. Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. ' les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.

</dd> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Non pris en charge.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TaskFolder**](taskfolder.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





