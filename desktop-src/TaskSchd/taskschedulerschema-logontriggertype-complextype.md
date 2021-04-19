---
title: Type complexe logonTriggerType
description: Définit les éléments enfants et les informations de séquencement pour l’élément LogonTrigger.
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- Planificateur de tâches de type complexe logonTriggerType
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a3f42eb94d14506d96348b803c8b1bc41737d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516101"
---
# <a name="logontriggertype-complex-type"></a>Type complexe logonTriggerType

Définit les éléments enfants et les informations de séquencement pour l’élément [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="logonTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
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



| Élément                                                               | Type                                                                    | Description                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Retard**](taskschedulerschema-delay-logontriggertype-element.md)   | duration                                                                | Intervalle de temps entre le moment où l’utilisateur ouvre une session et le moment où la tâche est démarrée.<br/>         |
| [**IDutilisateur**](taskschedulerschema-userid-logontriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Identificateur de l’utilisateur. La tâche est démarrée lorsque cet utilisateur ouvre une session sur l’ordinateur.<br/> |



## <a name="remarks"></a>Notes

Outre les éléments enfants définis ici, l’élément [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) utilise également les éléments enfants définis par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

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

 

 





