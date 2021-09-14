---
title: Type complexe idleSettingsType
description: Définit les éléments enfants et les informations de séquencement pour l’élément IdleSettings (settingsType).
ms.assetid: 0f50c4d6-fda9-42cc-8dab-4c9439fbea4b
keywords:
- Planificateur de tâches de type complexe idleSettingsType
topic_type:
- apiref
api_name:
- idleSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba5ffa3acb879aad095b5b136d882bb817eb0ab0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228773"
---
# <a name="idlesettingstype-complex-type"></a>Type complexe idleSettingsType

Définit les éléments enfants et les informations de séquencement pour l’élément [**IdleSettings (settingsType)**](taskschedulerschema-idlesettings-settingstype-element.md) .

``` syntax
<xs:complexType name="idleSettingsType">
    <xs:all>
        <xs:element name="Duration"
            default="PT10M"
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
        <xs:element name="WaitTimeout"
            default="PT1H"
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
        <xs:element name="StopOnIdleEnd"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                  | Type    | Description                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md)                |         | Spécifie la durée autorisée pour démarrer la tâche en état d’inactivité.<br/>                                                                                                                     |
| [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | boolean | La tâche est redémarrée dès qu’une condition d’inactivité démarre.<br/>                                                                                                                                             |
| [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | boolean | Spécifie que la tâche est terminée si la condition d’inactivité se termine avant que la durée d’inactivité soit dépassée.<br/>                                                                                                 |
| [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          |         | Spécifie la durée d’attente du démarrage d’une condition d’inactivité. Si aucune valeur n’est spécifiée pour cet élément, le service Planificateur de tâches attend indéfiniment qu’une condition d’inactivité se produise.<br/> |



## <a name="requirements"></a>Spécifications



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

 

 





