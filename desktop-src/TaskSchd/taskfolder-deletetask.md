---
title: Méthode TaskFolder. DeleteTask
description: Pour les scripts, supprime une tâche du dossier.
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- Planificateur de tâches de la méthode DeleteTask
- Méthode DeleteTask Planificateur de tâches, objet TaskFolder
- Planificateur de tâches objet TaskFolder, méthode DeleteTask
topic_type:
- apiref
api_name:
- TaskFolder.DeleteTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad4cf0a881a62cf5e9c1600653e5df58f3000f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742173"
---
# <a name="taskfolderdeletetask-method"></a>Méthode TaskFolder. DeleteTask

Pour les scripts, supprime une tâche du dossier.

## <a name="syntax"></a>Syntaxe


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom* \[ dans\]
</dt> <dd>

Nom de la tâche qui est spécifiée lors de l’inscription de la tâche. Le caractère'. 'ne peut pas être utilisé pour spécifier le dossier de la tâche actuelle et le'.. ' les caractères ne peuvent pas être utilisés pour spécifier le dossier de tâches parent dans le chemin d’accès.

</dd> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Non pris en charge. La valeur est 0

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

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

 

 





