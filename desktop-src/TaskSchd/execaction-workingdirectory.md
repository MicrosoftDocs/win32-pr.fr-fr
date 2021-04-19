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
ms.openlocfilehash: 28d4755b6f760ed1af75c676ecb70074c3ea7c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509912"
---
# <a name="execactionworkingdirectory-property"></a>ExecAction. WorkingDirectory, propriété

Pour les scripts, obtient ou définit le répertoire qui contient le fichier exécutable ou les fichiers utilisés par le fichier exécutable.

## <a name="syntax"></a>Syntaxe


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a>Valeur de la propriété

Le répertoire qui contient le fichier exécutable ou les fichiers utilisés par le fichier exécutable.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de code XML, le répertoire de travail de l’application est spécifié dans l’élément [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) du schéma planificateur de tâches.

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

 

 





