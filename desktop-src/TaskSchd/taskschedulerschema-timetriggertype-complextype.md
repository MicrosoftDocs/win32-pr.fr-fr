---
title: Type complexe timeTriggerType
description: Définit le type de base pour l’élément TimeTrigger.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- Planificateur de tâches de type complexe timeTriggerType
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f44f0959a9f67e4bfee0b0ef5dd7f095ffbadce
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734134"
---
# <a name="timetriggertype-complex-type"></a>Type complexe timeTriggerType

Définit le type de base pour l’élément [**timetrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                        | Type     | Description                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RandomDelay**](taskschedulerschema-randomdelay-timetriggertype-element.md) | duration | Spécifie le délai d’ajout aléatoire à l’heure de début du déclencheur. Le format de cette chaîne est `P<days>DT<hours>H<minutes>M<seconds>S` (par exemple, P2DT5S est un délai de 2 jours, 5 secondes). <br/> |



## <a name="remarks"></a>Remarques

Notez que cet élément n’ajoute pas d’éléments enfants à ceux définis par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types complexes de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





