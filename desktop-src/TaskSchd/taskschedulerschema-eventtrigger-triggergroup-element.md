---
title: Élément EventTrigger (triggerGroup)
description: Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- déclencheur d’événement Planificateur de tâches, élément
- EventTrigger, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- EventTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 555c8683933b2242d119fc00f29c6d0a33188f6404ca48a00e8a127dd59aa791
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424469"
---
# <a name="eventtrigger-triggergroup-element"></a>Élément EventTrigger (triggerGroup)

Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

L’élément **EventTrigger** est défini par [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Déclencheurs**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Spécifie les déclencheurs qui démarrent la tâche.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                              | Type                                                                     | Description                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Délai (eventTriggerType)**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                 | Spécifie la durée entre le moment où l’événement se produit et le moment où la tâche est démarrée.<br/>                                |
| [**Activé (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)             | boolean                                                                  | Spécifie que le déclencheur est activé.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)     | dateTime                                                                 | Spécifie la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/> |
| [**Répétition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)       | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md) | dateTime                                                                 | Spécifie la date et l’heure d’activation du déclencheur.<br/>                                                              |
| [**Abonnement (eventTriggerType)**](taskschedulerschema-subscription-eventtriggertype-element.md) | string                                                                   | Spécifie la requête XPath qui identifie l’événement qui déclenche le déclencheur.<br/>                                             |



## <a name="attributes"></a>Attributs



| Nom | Type | Description                           |
|------|------|---------------------------------------|
| Id   | ID   | Identificateur du déclencheur.<br/> |



## <a name="remarks"></a>Remarques

Vous pouvez créer au maximum 500 tâches avec des abonnements aux événements. Un abonnement aux événements qui interroge un grand nombre d’événements peut être utilisé pour déclencher une tâche qui utilise la même action en réponse aux événements journalisés.

Pour le développement de scripts, un déclencheur d’événement est défini par l’objet [**EventTrigger**](eventtrigger.md) .

Pour le développement C++, un déclencheur d’événement est défini par l’interface [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui utilise un déclencheur d’événement, consultez [exemple de déclencheur d’événements (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

