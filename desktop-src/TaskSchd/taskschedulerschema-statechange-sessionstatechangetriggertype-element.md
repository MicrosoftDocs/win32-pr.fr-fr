---
title: StateChange (sessionStateChangeTriggerType) (élément)
description: Contient le type de Terminal Server modification de session qui déclencherait un lancement de tâche.
ms.assetid: 0b17a4a5-caa7-4b58-a1a4-cbc7564838bb
keywords:
- StateChange, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- StateChange
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88b7e46b23cf6778379a967e03d8f168de3b18d20a734812bacdad940850136a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356331"
---
# <a name="statechange-sessionstatechangetriggertype-element"></a>StateChange (sessionStateChangeTriggerType) (élément)

Contient le type de Terminal Server modification de session qui déclencherait un lancement de tâche.

``` syntax
<xs:element name="StateChange"
    type="sessionStateChangeType"
 />
```

L’élément **StateChange** est défini par le type complexe [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                       | Dérivé de                                                                                           | Description                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Spécifie un déclencheur qui démarre une tâche quand une session de Terminal Server change d’État.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement C++, consultez la [**propriété StateChange de ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).

Pour le développement de scripts, consultez [**SessionStateChangeTrigger. StateChange**](sessionstatechangetrigger-statechange.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





