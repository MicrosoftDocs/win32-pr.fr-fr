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
ms.openlocfilehash: 2ddb55436a0a6980a8909da636a02ca59244ca85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384999"
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
| [**Retard**](taskschedulerschema-delay-registrationtriggertype-element.md) | duration | Spécifie la durée entre le moment où la tâche est inscrite et le moment où la tâche est démarrée.<br/> |



## <a name="remarks"></a>Notes

Outre les éléments enfants définis ici, l’élément [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) utilise également les éléments enfants définis par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





