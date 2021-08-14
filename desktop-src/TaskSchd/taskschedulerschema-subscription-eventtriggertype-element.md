---
title: Élément Subscription (eventTriggerType)
description: Spécifie la requête XPath qui identifie l’événement qui déclenche le déclencheur.
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- Planificateur de tâches d’élément d’abonnement
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ec45a9c240a9dd5d30d2089f98216fc165af13fe418424f5b85feed5e022b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131554"
---
# <a name="subscription-eventtriggertype-element"></a>Élément Subscription (eventTriggerType)

Spécifie la requête XPath qui identifie l’événement qui déclenche le déclencheur.

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

L’élément d' **abonnement** est défini par le type complexe [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                       | Dérivé de                                                                 | Description                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement de script, l’abonnement aux événements est spécifié par la propriété [**EventTrigger. subscription**](eventtrigger-subscription.md) .

Pour le développement C++, l’abonnement aux événements est spécifié par la propriété [**IEventTrigger :: Subscription**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) .

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

 

 





