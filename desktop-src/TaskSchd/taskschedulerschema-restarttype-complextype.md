---
title: Type complexe restartType
description: Définit les éléments enfants et les informations de séquence pour l’élément RestartOnFailure.
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- Planificateur de tâches de type complexe restartType
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 996debc2c8e3d7d00ca7b42facde582f918d72736426ed326691461d800f8562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516478"
---
# <a name="restarttype-complex-type"></a>Type complexe restartType

Définit les éléments enfants et les informations de séquence pour l’élément [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) .

``` syntax
<xs:complexType name="restartType">
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
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                              | Type | Description                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [**Count**](taskschedulerschema-count-restarttype-element.md)       |      | Nombre de tentatives de redémarrage de la tâche.<br/> |
| [**Intervalle**](taskschedulerschema-interval-restarttype-element.md) |      | Durée d’exécution de la tâche.<br/>      |



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

 

 





