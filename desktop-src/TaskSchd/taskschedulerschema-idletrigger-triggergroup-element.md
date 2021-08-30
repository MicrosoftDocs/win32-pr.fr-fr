---
title: Élément IdleTrigger (triggerGroup)
description: Spécifie un déclencheur qui démarre une tâche lorsque l’ordinateur passe en état d’inactivité.
ms.assetid: c3e317b5-d1a7-46de-ace5-e066452583d3
keywords:
- déclencheur Idle, élément XML
- Élément IdleTrigger Planificateur de tâches
topic_type:
- apiref
api_name:
- IdleTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1bb3986c94837c7970d178a90341c97e9857c51d346ce0007a491a86f42e82e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125829"
---
# <a name="idletrigger-triggergroup-element"></a>Élément IdleTrigger (triggerGroup)

Spécifie un déclencheur qui démarre une tâche lorsque l’ordinateur passe en état d’inactivité. Pour plus d’informations sur les conditions d’inactivité, consultez conditions d’inactivité de la [tâche](task-idle-conditions.md).

``` syntax
<xs:element name="IdleTrigger"
    type="idleTriggerType"
 />
```

L’élément **IdleTrigger** est défini par [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Déclencheurs**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Spécifie les déclencheurs qui démarrent la tâche.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                        | Type                                                                     | Description                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Activé (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Spécifie que le déclencheur est activé.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Spécifie la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Spécifie la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.<br/>                                   |
| [**Répétition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Spécifie la date et l’heure d’activation du déclencheur.<br/>                                                              |



## <a name="attributes"></a>Attributs



| Nom | Type   | Description                               |
|------|--------|-------------------------------------------|
| Id   | string | Identificateur du déclencheur.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement de scripts, un déclencheur inactif est spécifié à l’aide de l’objet [**IdleTrigger**](idletrigger.md) .

Pour le développement C++, un déclencheur inactif est spécifié à l’aide de l’interface [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) .

Les éléments enfants répertoriés ci-dessus sont définis par les types d’éléments complexes [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) . Ces éléments doivent être ajoutés dans l’ordre indiqué ci-dessous.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Activé (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Répétition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a>Exemples

Le code XML suivant définit un déclencheur inactif.


```XML
<IdleTrigger>
    <StartBoundary>2005-01-01T00:08:00</StartBoundary>
    <EndBounadry>2007-01-01T00:08:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
</IdleTrigger>
```



## <a name="requirements"></a>Configuration requise



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

 

