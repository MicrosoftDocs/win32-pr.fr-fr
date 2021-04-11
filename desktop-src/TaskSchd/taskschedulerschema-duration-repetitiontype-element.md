---
title: Élément Duration (repetitionType)
description: Spécifie la durée de répétition du modèle.
ms.assetid: a24f3827-18b2-465e-b132-77dce139e0d4
keywords:
- Élément Duration Planificateur de tâches
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3772abb0224b03db4985de126e1d9cc0058ab5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317506"
---
# <a name="duration-repetitiontype-element"></a>Élément Duration (repetitionType)

Spécifie la durée de répétition du modèle. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes). Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> . Si aucune valeur n’est spécifiée pour la durée, le modèle est répété indéfiniment. La valeur minimale est d’une minute.

``` syntax
<xs:element name="Duration"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
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

Pour les applications de script, la durée du modèle est spécifiée à l’aide de la propriété [**RepetitionPattern. Duration**](repetitionpattern-duration.md) .

Pour les applications C++, la durée du modèle est spécifiée à l’aide de la propriété [**IRepetitionPattern ::D figuration**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_duration) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un modèle de répétition pour un déclencheur.


```XML
<Repetition>
    <Interval></Interval>
    <Duration></Duration>
    <StopAtDurationEnd>true</StopAtDirationEnd>
</Repetition>
```



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

 

 





