---
title: ExecAction. WorkingDirectory, propriété
description: Pour les scripts, obtient ou définit le répertoire qui contient le fichier exécutable ou les fichiers utilisés par le fichier exécutable.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- Planificateur de tâches de la propriété WorkingDirectory
- Planificateur de tâches de la propriété WorkingDirectory, objet ExecAction
- Planificateur de tâches objet ExecAction, propriété WorkingDirectory
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 362b6cbb977e66a92425da1355f0747660d867f67aec0ad684f7e8e3956edc63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139442"
---
# <a name="execactionworkingdirectory-property"></a>ExecAction. WorkingDirectory, propriété

Pour les scripts, obtient ou définit le répertoire qui contient le fichier exécutable ou les fichiers utilisés par le fichier exécutable.

## <a name="syntax"></a>Syntaxe


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a>Valeur de la propriété

Le répertoire qui contient le fichier exécutable ou les fichiers utilisés par le fichier exécutable.

## <a name="remarks"></a>Remarques

Lors de la lecture ou de l’écriture de code XML, le répertoire de travail de l’application est spécifié dans l’élément [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) du schéma planificateur de tâches.

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

 

 





