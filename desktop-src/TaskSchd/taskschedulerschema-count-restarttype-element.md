---
title: Count (élément restartType)
description: Spécifie le nombre de tentatives de redémarrage de la tâche par le Planificateur de tâches.
ms.assetid: 67466c14-c9dd-49c8-a6ed-df7531fc63b8
keywords:
- Count, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 655f636b725e48749540d67710afa57b3c45c89c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011047"
---
# <a name="count-restarttype-element"></a>Count (élément restartType)

Spécifie le nombre de tentatives de redémarrage de la tâche par le Planificateur de tâches.

``` syntax
<xs:element name="Count">
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
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

Si cet élément est spécifié, l’élément [**Interval**](taskschedulerschema-interval-restarttype-element.md) doit également être spécifié pour indiquer au planificateur de tâches la durée de la tentative de redémarrage de la tâche.

Pour le développement C++, consultez la [**propriété RestartCount de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount).

Pour le développement de scripts, consultez [**TaskSettings. RestartCount**](tasksettings-restartcount.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





