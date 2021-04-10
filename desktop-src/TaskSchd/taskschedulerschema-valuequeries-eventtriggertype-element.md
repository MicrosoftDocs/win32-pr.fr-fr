---
title: Élément ValueQueries (eventTriggerType)
description: Contient une séquence d’éléments qui contiennent chacun un nom et une valeur de requête XPath.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- Élément ValueQueries Planificateur de tâches
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4448693c1c1ab19b2ea13050cc9ab817bdc25e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941820"
---
# <a name="valuequeries-eventtriggertype-element"></a>Élément ValueQueries (eventTriggerType)

Contient une séquence d’éléments qui contiennent chacun un nom et une valeur de requête XPath. Les requêtes sont appliquées à un événement renvoyé par l’abonnement à un événement spécifié dans l’élément [**subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) . Le nom de la valeur de requête XPath peut être utilisé en tant que variable dans la section action d’une tâche.

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

L’élément **ValueQueries** est défini par le type complexe [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                      | Dérivé de                                                                 | Description                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger (triggerGroup)**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété ValueQueries de IEventTrigger**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).

Pour le développement de scripts, consultez [**EventTrigger. ValueQueries**](eventtrigger-valuequeries.md).

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui spécifie un déclencheur d’événement à l’aide de cet élément, consultez [exemple de déclencheur d’événements (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

