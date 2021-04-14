---
title: Objet TaskDefinition
description: Objet de script qui définit tous les composants d’une tâche, tels que les paramètres de tâche, les déclencheurs, les actions et les informations d’inscription.
ms.assetid: d5887024-21af-40cf-a97d-f695f60394d9
keywords:
- Objet TaskDefinition Planificateur de tâches
- Planificateur de tâches d’objets TaskDefinition, Description
topic_type:
- apiref
api_name:
- TaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d911218f64b386c08091f981903126f7506e3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508774"
---
# <a name="taskdefinition-object"></a>Objet TaskDefinition

Objet de script qui définit tous les composants d’une tâche, tels que les paramètres de tâche, les déclencheurs, les actions et les informations d’inscription.

## <a name="members"></a>Membres

L’objet **TaskDefinition** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **TaskDefinition** a ces propriétés.



| Propriété                                                               | Type d’accès           | Description                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Actions**](taskdefinition-actions.md)<br/>                   | Lecture/écriture<br/> | Obtient ou définit une collection d’actions exécutées par la tâche.<br/>                                                                                                         |
| [**Données**](taskdefinition-data.md)<br/>                         | Lecture/écriture<br/> | Obtient ou définit les données associées à la tâche. Ces données sont ignorées par le service Planificateur de tâches, mais elles sont utilisées par des tiers qui souhaitent étendre le format des tâches.<br/> |
| [**Directeur**](taskdefinition-principal.md)<br/>               | Lecture/écriture<br/> | Obtient ou définit le principal de la tâche qui fournit les informations d’identification de sécurité pour la tâche.<br/>                                                                                 |
| [**RegistrationInfo**](taskdefinition-registrationinfo.md)<br/> | Lecture/écriture<br/> | Obtient ou définit les informations d’inscription utilisées pour décrire une tâche, telles que la description de la tâche, l’auteur de la tâche et la date à laquelle la tâche est inscrite.<br/> |
| [**Paramètres**](taskdefinition-settings.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit les paramètres qui définissent la façon dont le service de Planificateur de tâches exécute la tâche.<br/>                                                                                      |
| [**Déclencheurs**](taskdefinition-triggers.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit une collection de déclencheurs utilisés pour démarrer une tâche.<br/>                                                                                                         |
| [**XmlText**](taskdefinition-xmltext.md)<br/>                   | Lecture/écriture<br/> | Obtient ou définit la définition XML de la tâche.<br/>                                                                                                                       |



 

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de votre propre code XML pour une tâche, une définition de tâche est spécifiée à l’aide de l’élément [**Task**](taskschedulerschema-task-element.md) du schéma planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md) , [exemple de déclenchement d’événements (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), exemple de [déclencheur quotidien (script)](daily-trigger-example--scripting-.md), [exemple de déclencheur d’inscription (](registration-trigger-example--scripting-.md)script), exemple de [déclencheur hebdomadaire (](weekly-trigger-example--scripting-.md)script), exemple de [déclencheur LOGON (script)](logon-trigger-example--scripting-.md)ou [exemple de déclencheur de démarrage](boot-trigger-example--scripting-.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





