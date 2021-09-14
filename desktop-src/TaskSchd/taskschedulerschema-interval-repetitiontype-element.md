---
title: Interval (élément repetitionType)
description: Spécifie la durée entre chaque redémarrage de la tâche.
ms.assetid: 28c6475a-88e3-44ac-92c7-6f463e8460c9
keywords:
- Élément Interval Planificateur de tâches
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bfb87884438f1a39a5bd6f08eb9bb855311eb5d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228762"
---
# <a name="interval-repetitiontype-element"></a>Interval (élément repetitionType)

Spécifie la durée entre chaque redémarrage de la tâche. Le format de cette chaîne est `P<days>DT<hours>H<minutes>M<seconds>S` (par exemple, « PT5M » est de 5 minutes, « PT1H » est 1 heure et « PT20M » est 20 minutes). La durée maximale autorisée est de 31 jours, et la durée minimale autorisée est de 1 minute.

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément est défini par le type complexe [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                      | Dérivé de                                                             | Description                                                                                                               |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Répétition**](taskschedulerschema-repetition-triggerbasetype-element.md) | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de script, l’intervalle du modèle de répétition est spécifié à l’aide de la propriété [**RepetitionPattern. Interval**](repetitionpattern-interval.md) .

Pour le développement C++, l’intervalle du modèle de répétition est spécifié à l’aide de la propriété [**IRepetitionPattern :: Interval**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_interval) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui utilise un intervalle de répétition, consultez [exemple de déclencheur quotidien (XML)](daily-trigger-example--xml-.md).

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

 

 





