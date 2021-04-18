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
ms.openlocfilehash: 4f5f10ce90861c76d0a751c54e8282269b7a8986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512613"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





