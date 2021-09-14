---
title: Élément Delay (sessionStateChangeTriggerType)
description: Contient une valeur qui indique la durée de délai pour l’heure de début d’une tâche, lorsqu’un changement d’état de session Terminal Server est détecté.
ms.assetid: 7fb87c4c-0b69-4c5b-b038-d61fb7c4ab9a
keywords:
- Retarder l’élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03f230465f2e2b49ce83f1af358dfa1f84f21433
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013406"
---
# <a name="delay-sessionstatechangetriggertype-element"></a>Élément Delay (sessionStateChangeTriggerType)

Contient une valeur qui indique la durée de délai pour l’heure de début d’une tâche, lorsqu’un changement d’état de session Terminal Server est détecté. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes). Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

L’élément **delay** est défini par le type complexe [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                       | Dérivé de                                                                                           | Description                                                                                      |
|-------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Spécifie un déclencheur qui démarre une tâche quand une session de Terminal Server change d’État. <br/> |



## <a name="remarks"></a>Notes

Pour le développement de script, le délai de déclenchement du changement d’état de session est spécifié à l’aide de la propriété [**SessionStateChangeTrigger. Delay**](sessionstatechangetrigger-delay.md) .

Pour le développement C++, le délai de déclenchement du changement d’état de session est spécifié à l’aide [**de la propriété Delay de ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





