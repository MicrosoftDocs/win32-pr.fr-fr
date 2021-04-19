---
title: Type complexe eventTriggerType
description: Définit les éléments enfants et les informations de séquencement pour l’élément EventTrigger.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- Planificateur de tâches de type complexe eventTriggerType
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16c3d4257d89ebb8d0efb6dadcd3ac466b929c9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106538612"
---
# <a name="eventtriggertype-complex-type"></a>Type complexe eventTriggerType

Définit les éléments enfants et les informations de séquencement pour l’élément [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="eventTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Subscription"
                    type="nonEmptyString"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="ValueQueries"
                    type="namedValues"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                           | Type                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Retard**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                | Spécifie la durée entre le moment où l’événement se produit et le moment où la tâche est démarrée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Abonnement**](taskschedulerschema-subscription-eventtriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Spécifie la requête XPath qui identifie l’événement qui déclenche le déclencheur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md)      | Spécifie une séquence d’éléments qui contiennent chacun un nom et une valeur de requête XPath. Les requêtes sont appliquées à un événement renvoyé par l’abonnement à un événement spécifié dans l’élément [**subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) . Le nom de la valeur de requête XPath peut être utilisé en tant que variable dans l’élément [**Body**](taskschedulerschema-body-showmessagetype-element.md) de la section d’action [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) d’une tâche. <br/> |



## <a name="remarks"></a>Notes

En plus de l’élément enfant défini ici, l’élément [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) utilise également des éléments enfants définis par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





