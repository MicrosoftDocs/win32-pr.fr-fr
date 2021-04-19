---
title: Élément Delay (eventTriggerType)
description: Spécifie la durée entre le moment où l’événement se produit et le moment où la tâche est démarrée.
ms.assetid: b38bebc7-9818-41f0-a277-cb0e63c28d86
keywords:
- Retarder l’élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de1117ff4f7e0f823b1b213721521e1b526125bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517333"
---
# <a name="delay-eventtriggertype-element"></a>Élément Delay (eventTriggerType)

Spécifie la durée entre le moment où l’événement se produit et le moment où la tâche est démarrée. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes). Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

L’élément **delay** est défini par le type complexe [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                       | Dérivé de                                                                 | Description                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Spécifie un déclencheur qui démarre une tâche lorsqu’un événement système se produit.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de scripts, le délai de déclenchement des événements est spécifié par la propriété [**EventTrigger. Delay**](eventtrigger-delay.md) .

Pour le développement C++, le délai de déclenchement des événements est spécifié par la propriété [**IEventTrigger ::D Nouv**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





