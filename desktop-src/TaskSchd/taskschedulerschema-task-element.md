---
title: Task, élément
description: Définit la tâche qui est effectuée par le service Planificateur de tâches.
ms.assetid: 103a332a-8620-4e0c-81b5-4782d85fc391
keywords:
- Élément Task Planificateur de tâches
topic_type:
- apiref
api_name:
- Task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38bac482f8546028d21db913e31dc4152f19f599
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843257"
---
# <a name="task-element"></a>Task, élément

Définit la tâche qui est effectuée par le service Planificateur de tâches.

``` syntax
<xs:element name="Task"
    type="taskType"
>
    <xs:key name="PrincipalKey">
        <xs:selector
            xpath="td:Principals/td:Principal"
         />
        <xs:field
            xpath="@id"
         />
    </xs:key>
    <xs:keyref name="ContextKeyRef">
        <xs:selector
            xpath="td:Actions"
         />
        <xs:field
            xpath="@Context"
         />
    </xs:keyref>
    <xs:unique name="UniqueId">
        <xs:selector
            xpath="td:Principals/td:Principal|td:Triggers/td:BootTrigger|td:Triggers/td:RegistrationTrigger|td:Triggers/td:IdleTrigger|td:Triggers/td:TimeTrigger|td:Triggers/td:EventTrigger|td:Triggers/td:LogonTrigger|td:Triggers/td:SessionStateChangeTrigger|td:Triggers/td:CalendarTrigger|td:Actions/td:Exec|td:Actions/td:ComHandler|td:Actions/td:SendEmail"
         />
        <xs:field
            xpath="@id"
         />
    </xs:unique>
</xs:element>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                           | Type                                                                                 | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**Actions**](taskschedulerschema-actions-tasktype-element.md)                   | [**actionsType**](taskschedulerschema-actionstype-complextype.md)                   | Spécifie les actions effectuées par la tâche.<br/>                                                                             |
| [**Données**](taskschedulerschema-data-tasktype-element.md)                         | [**Décimal**](taskschedulerschema-datatype-complextype.md)                         | Spécifie des données supplémentaires associées à la tâche, mais qui, sinon, ne sont pas utilisées par le service Planificateur de tâches.<br/>         |
| [**Principaux**](taskschedulerschema-principals-tasktype-element.md)             | [**principalsType**](taskschedulerschema-principalstype-complextype.md)             | Spécifie les contextes de sécurité qui peuvent être utilisés pour exécuter la tâche.<br/>                                                        |
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.<br/> |
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md)                 | [**settingsType**](taskschedulerschema-settingstype-complextype.md)                 | Spécifie les paramètres utilisés par le Planificateur de tâches pour effectuer la tâche.<br/>                                                 |
| [**Déclencheurs**](taskschedulerschema-triggers-tasktype-element.md)                 | [**triggersType**](taskschedulerschema-triggerstype-complextype.md)                 | Spécifie les déclencheurs qui démarrent la tâche.<br/>                                                                              |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).

Pour le développement de scripts, consultez [**TaskDefinition**](taskdefinition.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





