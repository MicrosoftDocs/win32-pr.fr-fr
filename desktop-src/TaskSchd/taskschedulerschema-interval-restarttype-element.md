---
title: Interval (élément restartType)
description: Spécifie la durée pendant laquelle le Planificateur de tâches tente de redémarrer la tâche.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
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
ms.openlocfilehash: c97e754e0b29a43d6ba419bd806404fe1b85b2b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941767"
---
# <a name="interval-restarttype-element"></a>Interval (élément restartType)

Spécifie la durée pendant laquelle le Planificateur de tâches tente de redémarrer la tâche. Le format de cette chaîne est P <days> DT <hours> H <minutes> M <seconds> S (par exemple, « PT5M » est de 5 minutes, « PT1H » est 1 heure et « PT20M » est de 20 minutes). La durée maximale autorisée est de 31 jours, et la durée minimale autorisée est de 1 minute.

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

L’élément est défini par le type complexe [**restartType**](taskschedulerschema-restarttype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                               | Dérivé de                                                       | Description                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md) | [**restartType**](taskschedulerschema-restarttype-complextype.md) | Spécifie que l’Planificateur de tâches tentera de redémarrer la tâche si elle échoue pour une raison quelconque.<br/> |



## <a name="remarks"></a>Notes

Si cet élément est spécifié, l’élément [**Count**](taskschedulerschema-count-restarttype-element.md) doit également être spécifié pour indiquer au planificateur de tâches combien de fois il doit essayer de redémarrer la tâche.

Pour le développement C++, consultez la [**propriété RestartInterval de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval).

Pour le développement de scripts, consultez [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





