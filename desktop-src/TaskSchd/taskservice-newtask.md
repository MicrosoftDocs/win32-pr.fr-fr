---
title: TaskService. NewTask, méthode
description: Pour les scripts, retourne un objet de définition de tâche vide à remplir avec les paramètres et les propriétés, puis inscrit à l’aide de la méthode TaskFolder. RegisterTaskDefinition.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- Méthode NewTask Planificateur de tâches
- Méthode NewTask Planificateur de tâches, objet TaskService
- Objet TaskService Planificateur de tâches, méthode NewTask
topic_type:
- apiref
api_name:
- TaskService.NewTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22da6f62f59bf24ded0eed9dea21e3a1a9d1c3e7ecc36fb6f425f58124aee71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990929"
---
# <a name="taskservicenewtask-method"></a>TaskService. NewTask, méthode

Pour les scripts, retourne un objet de définition de tâche vide à remplir avec les paramètres et les propriétés, puis inscrit à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .

## <a name="syntax"></a>Syntaxe


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Ce paramètre est réservé pour une utilisation ultérieure et doit avoir la valeur 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Définition de la tâche qui spécifie toutes les informations requises pour créer une nouvelle tâche.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





