---
title: Type complexe sessionStateChangeTriggerType
description: Définit les éléments utilisés pour créer un déclencheur de tâche pour la connexion à la console ou la déconnexion, la connexion à distance ou la déconnexion ou les notifications de verrouillage ou de déverrouillage de station de travail
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- Planificateur de tâches de type complexe sessionStateChangeTriggerType
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8eb3ad02aef3f5bbbc078f8eafa52f3439819cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317497"
---
# <a name="sessionstatechangetriggertype-complex-type"></a>Type complexe sessionStateChangeTriggerType

Définit les éléments utilisés pour créer un déclencheur de tâche pour la connexion à la console ou la déconnexion, la connexion à distance ou la déconnexion ou les notifications de verrouillage ou de déverrouillage de station de travail

``` syntax
<xs:complexType name="sessionStateChangeTriggerType">
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
                <xs:element name="StateChange"
                    type="sessionStateChangeType"
                    minOccurs="1"
                    maxOccurs="1"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                      | Type                                                                                    | Description                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Retard**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Spécifie une valeur qui indique la durée du délai avant le démarrage d’une tâche lorsqu’une modification d’état de session Terminal Server est détectée.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Spécifie le type de Terminal Server modification de session qui déclencherait un lancement de tâche.<br/>                                                     |
| [**IDutilisateur**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | Spécifie l’utilisateur pour la session de Terminal Server. Lorsqu’une modification d’état de session est détectée pour cet utilisateur, une tâche est démarrée.<br/>              |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





