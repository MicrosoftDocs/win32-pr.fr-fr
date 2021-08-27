---
title: Élément SessionStateChangeTrigger (triggerGroup)
description: Spécifie un déclencheur qui démarre une tâche quand une session de Terminal Server change d’État.
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- Élément SessionStateChangeTrigger Planificateur de tâches
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d22b2f47584f437c01575ffecfb6d5c25e312b9584ba46abc9d6997e14187eaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099819"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a>Élément SessionStateChangeTrigger (triggerGroup)

Spécifie un déclencheur qui démarre une tâche quand une session de Terminal Server change d’État.

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

L’élément **SessionStateChangeTrigger** est défini par [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Déclencheurs**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Spécifie les déclencheurs qui démarrent la tâche.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                      | Type                                                                                    | Description                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Retarder**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Spécifie une valeur qui indique la durée du délai avant le démarrage d’une tâche lorsqu’une modification d’état de session Terminal Server est détectée.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Spécifie le type de Terminal Server modification de session qui déclencherait un lancement de tâche.<br/>                                                     |
| [**IDutilisateur**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | Spécifie l’utilisateur pour la session de Terminal Server. Lorsqu’une modification d’état de session est détectée pour cet utilisateur, une tâche est démarrée.<br/>              |



## <a name="remarks"></a>Remarques

Pour le développement de script, un déclencheur de changement d’état de session est spécifié à l’aide de l’objet [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) .

Pour le développement C++, un déclencheur de changement d’état de session est spécifié à l’aide de l’interface [**ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





