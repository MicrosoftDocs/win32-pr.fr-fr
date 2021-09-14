---
title: Élément principal (taskType)
description: Spécifie les contextes de sécurité qui peuvent être utilisés pour exécuter la tâche.
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- Élément principals Planificateur de tâches
topic_type:
- apiref
api_name:
- Principals
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2385d7ff766d72300a402fccfae8eb7338b89f87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920375"
---
# <a name="principals-tasktype-element"></a>Élément principal (taskType)

Spécifie les contextes de sécurité qui peuvent être utilisés pour exécuter la tâche.

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

L’élément **principals** est défini par le type complexe [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                          | Dérivé de                                                 | Description                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Tâche**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Définit la tâche qui est effectuée par le service Planificateur de tâches.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                  | Type                                                                   | Description                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Spécifie les informations d’identification de sécurité pour un principal.<br/> |



## <a name="remarks"></a>Notes

Vous pouvez spécifier jusqu’à 32 principaux pour une tâche.

Pour le développement de scripts, les principaux d’une tâche sont spécifiés à l’aide de la propriété [**TaskDefinition. principal**](taskdefinition-principal.md) .

Pour le développement C++, les principaux d’une tâche sont spécifiés à l’aide [**de la propriété principal de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).

## <a name="examples"></a>Exemples

Le code XML suivant définit deux principaux : un identificateur d’utilisateur et un principal d’identificateur de groupe pour la tâche.


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





