---
title: Objet ExecAction
description: Objet de script qui représente une action qui exécute une opération de ligne de commande.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- Planificateur de tâches d’exécution de l’action, interface
- Objet ExecAction Planificateur de tâches
- Planificateur de tâches d’objets ExecAction, Description
topic_type:
- apiref
api_name:
- ExecAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140ff991bd26f779beee7407666572d8649bd9f1a2718b719713770745157656
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072659"
---
# <a name="execaction-object"></a>Objet ExecAction

Objet de script qui représente une action qui exécute une opération de ligne de commande.

## <a name="members"></a>Membres

L’objet **ExecAction** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **ExecAction** a ces propriétés.



| Propriété                                                            | Type d’accès           | Description                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | Lecture/écriture<br/> | Obtient ou définit les arguments associés à l’opération de ligne de commande.<br/>                                                 |
| [**Identifi**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | Lecture/écriture<br/> | Hérité de l’objet d' [**action**](action.md) . Obtient ou définit l’identificateur de l’action.<br/>                         |
| [**Chemin**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | Lecture/écriture<br/> | Obtient ou définit le chemin d’accès à un fichier exécutable.<br/>                                                                           |
| [**Type**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | Lecture seule<br/>  | Hérité de l’objet d' [**action**](action.md) . Obtient le type d'action.<br/>                                       |
| [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | Lecture/écriture<br/> | Obtient ou définit le répertoire qui contient le fichier exécutable ou les fichiers utilisés par le fichier exécutable.<br/> |



 

## <a name="remarks"></a>Remarques

Si les variables d’environnement sont utilisées dans les propriétés [**path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)ou [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) , les valeurs des variables d’environnement sont mises en cache et utilisées lors du lancement du Taskeng.exe (le moteur de tâches). Les modifications apportées aux variables d’environnement qui se produisent après le lancement du moteur de tâche ne sont pas utilisées par le moteur de tâche.

Cette action effectue une opération de ligne de commande. Par exemple, l’action peut exécuter un script ou lancer un exécutable.

Lors de la lecture ou de l’écriture de données XML, une action d’exécution est spécifiée dans l’élément [**Exec**](taskschedulerschema-exec-actiongroup-element.md) du schéma planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





