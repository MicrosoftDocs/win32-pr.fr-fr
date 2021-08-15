---
title: Élément Delay (logonTriggerType)
description: Intervalle de temps entre le moment où l’utilisateur ouvre une session et le moment où la tâche est démarrée.
ms.assetid: daab29f7-5d05-4e6d-a0c0-7b83b4d0b941
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
ms.openlocfilehash: 1bd18652630ad14f9b888db6a810d8da1eb42a18fb9d2caa6726414aa9054702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357134"
---
# <a name="delay-logontriggertype-element"></a>Élément Delay (logonTriggerType)

Intervalle de temps entre le moment où l’utilisateur ouvre une session et le moment où la tâche est démarrée. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes). Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

L’élément **delay** est défini par le type complexe [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                       | Dérivé de                                                                 | Description                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) | Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement de scripts, le délai de déclenchement de connexion est spécifié à l’aide de la propriété [**LogonTrigger. Delay**](logontrigger-delay.md) .

Pour le développement C++, l’identificateur d’utilisateur du déclencheur LOGON est spécifié à l’aide de la propriété [**ILogonTrigger ::D Nouv**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





