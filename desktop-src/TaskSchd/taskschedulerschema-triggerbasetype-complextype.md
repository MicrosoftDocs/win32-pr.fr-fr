---
title: Type complexe triggerBaseType
description: Définit l’attribut, les éléments enfants de base et les informations de séquencement pour tous les types complexes de déclencheur.
ms.assetid: 1a2d004a-6f52-42b7-b0d0-ace8d27e9166
keywords:
- Planificateur de tâches de type complexe triggerBaseType
topic_type:
- apiref
api_name:
- triggerBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 21eed68ff260d199a46adabc0e560533658c6cc1398d00f9507b80b40fb69955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611010"
---
# <a name="triggerbasetype-complex-type"></a>Type complexe triggerBaseType

Définit l’attribut, les éléments enfants de base et les informations de séquencement pour tous les types complexes de déclencheur.

``` syntax
<xs:complexType name="triggerBaseType"
    abstract="true"
>
    <xs:sequence>
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="EndBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Repetition"
            type="repetitionType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                      | Type                                                                     | Description                                                                                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**activé**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Spécifie que le déclencheur est activé.<br/>                                                                      |
| [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Date et heure de désactivation du déclencheur.<br/>                                                          |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Spécifie l’intervalle auquel le déclencheur peut démarrer la tâche.<br/>                                                 |
| [**Répétition**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition une fois que le déclencheur est activé.<br/> |
| [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Date et heure d’activation du déclencheur.<br/>                                                            |



## <a name="attributes"></a>Attributs



| Nom | Type | Description                           |
|------|------|---------------------------------------|
| id   | ID   | Identificateur du déclencheur.<br/> |



## <a name="remarks"></a>Remarques

Les types complexes de déclencheurs sont les suivants.

-   [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md)
-   [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md)
-   [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md)
-   [**idleTriggerType**](taskschedulerschema-idletriggertype-complextype.md)
-   [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md)
-   [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md)
-   [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md)

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

 

 





