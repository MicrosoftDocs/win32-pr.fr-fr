---
title: Type complexe bootTriggerType
description: Définit l’élément enfant et les informations de séquencement pour l’élément BootTrigger.
ms.assetid: 36ade928-7640-4f91-ab76-18398b0cd65f
keywords:
- Planificateur de tâches de type complexe bootTriggerType
topic_type:
- apiref
api_name:
- bootTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc0b04bfaf08ecee87d02a2b410fd1df2fbbe584d5649a5e9fe2ea2e5efacebd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131858"
---
# <a name="boottriggertype-complex-type"></a>Type complexe bootTriggerType

Définit l’élément enfant et les informations de séquencement pour l’élément [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="bootTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                            | Type     | Description                                                                                 |
|--------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------|
| [**Retarder**](taskschedulerschema-delay-boottriggertype-element.md) | duration | Intervalle de temps entre le démarrage du système et le déclenchement du déclencheur. <br/> |



## <a name="remarks"></a>Remarques

En plus de l’élément enfant défini ici, l’élément [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) utilise également les éléments enfants définis par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types complexes de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





