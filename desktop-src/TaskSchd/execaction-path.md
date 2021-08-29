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
ms.openlocfilehash: d363485db56634c39a4a12e153feb740b0c21a2b6a3ef9499754de753c6236f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011449"
---
# <a name="execactionpath-property"></a>ExecAction. Path, propriété

Pour les scripts, obtient ou définit le chemin d’accès à un fichier exécutable.

## <a name="syntax"></a>Syntaxe


```VB
ExecAction.Path As String
```



## <a name="property-value"></a>Valeur de la propriété

Chemin d’accès au fichier exécutable à exécuter par l’action.

## <a name="remarks"></a>Remarques

Cette action effectue une opération de ligne de commande. Par exemple, l’action peut exécuter un script ou lancer un exécutable.

Lors de la lecture ou de l’écriture de données XML, le chemin d’accès de l’opération de ligne de commande est spécifié dans l’élément [**Command**](taskschedulerschema-command-exectype-element.md) du schéma planificateur de tâches.

Le chemin d’accès est vérifié pour s’assurer qu’il est valide lorsque la tâche est inscrite, et non lorsque cette propriété est définie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





