---
title: Type complexe repetitionType
description: Définit les éléments enfants et les informations de séquence pour l’élément de répétition (triggerBaseType).
ms.assetid: d2b4b840-3a69-4ff8-ac32-6ec76e7e8788
keywords:
- Planificateur de tâches de type complexe repetitionType
topic_type:
- apiref
api_name:
- repetitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d45f83be8ab8b37211224ec9f284a71cdde6bfc06032c5d05df9e5dee8bf4ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772089"
---
# <a name="repetitiontype-complex-type"></a>Type complexe repetitionType

Définit les éléments enfants et les informations de séquence pour l’élément de [**répétition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md) .

``` syntax
<xs:complexType name="repetitionType">
    <xs:all>
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
        <xs:element name="StopAtDurationEnd"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                   | Type    | Description                                                                                                            |
|-------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------|
| [**Duration**](taskschedulerschema-duration-repetitiontype-element.md)                   |         | Spécifie la durée de répétition du modèle. Si aucune valeur n’est spécifiée, le modèle est répété indéfiniment.<br/> |
| [**Défini**](taskschedulerschema-interval-repetitiontype-element.md)                   |         | Spécifie la durée entre chaque redémarrage de la tâche.<br/>                                              |
| [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | boolean | Spécifie qu’une instance en cours d’exécution de la tâche est arrêtée à la fin de la durée du modèle de répétition.<br/>     |



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

 

 





