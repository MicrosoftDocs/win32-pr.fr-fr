---
title: Type complexe registrationTriggerType
description: Définit des éléments enfants et des informations de séquencement pour l’élément RegistrationTrigger.
ms.assetid: 3663c015-67cf-4775-a1a6-4429cce93b96
keywords:
- Planificateur de tâches de type complexe registrationTriggerType
topic_type:
- apiref
api_name:
- registrationTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dab91ecc0eed065a4ce3eea9d64bebae2e10560a43ab57308ea68e82dc17dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772279"
---
# <a name="registrationtriggertype-complex-type"></a>Type complexe registrationTriggerType

Définit des éléments enfants et des informations de séquencement pour l’élément [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="registrationTriggerType">
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



| Élément                                                                    | Type     | Description                                                                                               |
|----------------------------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------|
| [**Retarder**](taskschedulerschema-delay-registrationtriggertype-element.md) | duration | Spécifie la durée entre le moment où la tâche est inscrite et le moment où la tâche est démarrée.<br/> |



## <a name="remarks"></a>Remarques

Outre les éléments enfants définis ici, l’élément [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) utilise également les éléments enfants définis par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





