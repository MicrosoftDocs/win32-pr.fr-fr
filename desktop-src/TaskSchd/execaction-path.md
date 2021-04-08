---
title: ExecAction. Path, propriété
description: Pour les scripts, obtient ou définit le chemin d’accès à un fichier exécutable.
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- Propriété Path Planificateur de tâches
- Propriété Path Planificateur de tâches, objet ExecAction
- Planificateur de tâches objet ExecAction, propriété Path
topic_type:
- apiref
api_name:
- ExecAction.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20e1dcd8cd9700f961eb944c7be3168582b8c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740860"
---
# <a name="execactionpath-property"></a>ExecAction. Path, propriété

Pour les scripts, obtient ou définit le chemin d’accès à un fichier exécutable.

## <a name="syntax"></a>Syntaxe


```VB
ExecAction.Path As String
```



## <a name="property-value"></a>Valeur de la propriété

Chemin d’accès au fichier exécutable à exécuter par l’action.

## <a name="remarks"></a>Notes

Cette action effectue une opération de ligne de commande. Par exemple, l’action peut exécuter un script ou lancer un exécutable.

Lors de la lecture ou de l’écriture de données XML, le chemin d’accès de l’opération de ligne de commande est spécifié dans l’élément [**Command**](taskschedulerschema-command-exectype-element.md) du schéma planificateur de tâches.

Le chemin d’accès est vérifié pour s’assurer qu’il est valide lorsque la tâche est inscrite, et non lorsque cette propriété est définie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





