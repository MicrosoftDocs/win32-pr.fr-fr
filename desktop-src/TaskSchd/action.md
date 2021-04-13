---
title: Objet d’action
description: Objet de script qui fournit les propriétés communes qui sont héritées par tous les objets d’action.
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- Objet d’action Planificateur de tâches
- Planificateur de tâches d’objet d’action, Description
topic_type:
- apiref
api_name:
- Action
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236b26cc4cfcd10f1e6e6094e4b69928343a9ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508882"
---
# <a name="action-object"></a>Objet d’action

Objet de script qui fournit les propriétés communes qui sont héritées par tous les objets d’action. Un objet d’action est créé par la méthode [**ActionCollection. Create**](actioncollection-create.md) .

## <a name="members"></a>Membres

L’objet d' **action** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet d' **action** a ces propriétés.



| Propriété                               | Type d’accès           | Description                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [**Identifi**](action-id.md)<br/>     | Lecture/écriture<br/> | Obtient ou définit l’identificateur de l’action.<br/> |
| [**Entrer**](action-type.md)<br/> | Lecture seule<br/>  | Obtient le type d'action.<br/>               |



 

## <a name="remarks"></a>Notes

Pour plus d’informations sur la façon dont les actions et les tâches fonctionnent ensemble, consultez [actions des tâches](task-actions.md). Le tableau suivant contient les objets de script qui représentent les actions qui peuvent être effectuées :



| API                                            | Description                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**ComHandlerAction**](comhandleraction.md)   | Représente une action qui déclenche un gestionnaire.                   |
| [**ExecAction**](execaction.md)               | Représente une action qui exécute une opération de ligne de commande. |
| [**EmailAction**](emailaction.md)             | Représente une action qui envoie un message électronique.            |
| [**ShowMessageAction**](showmessageaction.md) | Représente une action qui affiche une boîte de message.               |



 

Lors de la lecture ou de l’écriture de données XML, les actions d’une tâche sont spécifiées dans l’élément [**actions**](taskschedulerschema-actions-tasktype-element.md) du schéma planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md) , [exemple de déclenchement d’événements (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), exemple de [déclencheur quotidien (script)](daily-trigger-example--scripting-.md), [exemple de déclencheur d’inscription (](registration-trigger-example--scripting-.md)script), exemple de [déclencheur hebdomadaire (](weekly-trigger-example--scripting-.md)script), exemple de [déclencheur LOGON (script)](logon-trigger-example--scripting-.md)ou [exemple de déclencheur de démarrage](boot-trigger-example--scripting-.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches des objets de script](task-scheduler-objects.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





