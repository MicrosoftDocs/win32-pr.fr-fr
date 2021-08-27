---
title: Élément RegistrationTrigger (triggerGroup)
description: Spécifie un déclencheur qui démarre une tâche lorsque la tâche est inscrite.
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- Planificateur de tâches de déclencheur d’inscription, élément XML
- Élément RegistrationTrigger Planificateur de tâches
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 548ffec6bf5982aac407905d944d029b222b741c0c03fe66645f68e771c87342
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099969"
---
# <a name="registrationtrigger-triggergroup-element"></a>Élément RegistrationTrigger (triggerGroup)

Spécifie un déclencheur qui démarre une tâche lorsque la tâche est inscrite.

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

L’élément **RegistrationTrigger** est défini par le type complexe [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Déclencheurs**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Spécifie les déclencheurs qui démarrent la tâche.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                        | Type                                                                     | Description                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Délai (registrationTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)                   | duration                                                                 | Spécifie la durée entre le moment où la tâche est inscrite et le moment où la tâche est démarrée.<br/>                          |
| [**Activé (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Spécifie que le déclencheur est activé.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Spécifie la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Spécifie la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.<br/>                                   |
| [**Répétition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Spécifie la date et l’heure d’activation du déclencheur.<br/>                                                              |



## <a name="attributes"></a>Attributs



| Nom | Type | Description                           |
|------|------|---------------------------------------|
| Id   | ID   | Identificateur du déclencheur.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement de scripts, un déclencheur d’inscription est spécifié à l’aide de l’objet [**RegistrationTrigger**](registrationtrigger.md) .

Pour le développement C++, un déclencheur d’inscription est spécifié à l’aide de l’interface [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) .

Les éléments enfants répertoriés ci-dessus sont définis par les types d’éléments complexes [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) et [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) . Ces éléments doivent être ajoutés dans l’ordre indiqué ci-dessous.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Activé (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Répétition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**Délai (registrationTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui spécifie un déclencheur de démarrage, consultez [exemple de déclencheur d’inscription (XML)](registration-trigger-example--xml-.md).

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

 

 





