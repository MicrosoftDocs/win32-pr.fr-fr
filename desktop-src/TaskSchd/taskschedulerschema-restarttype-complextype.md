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
ms.openlocfilehash: 7f83dcac376fcdd8d2059649350502111f5a732f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519129"
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
| [**Saut**](taskschedulerschema-count-restarttype-element.md)       |      | Nombre de tentatives de redémarrage de la tâche.<br/> |
| [**Défini**](taskschedulerschema-interval-restarttype-element.md) |      | Durée d’exécution de la tâche.<br/>      |



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

 

 





