---
title: Élément RestartOnIdle (idleSettingsType)
description: Spécifie si la tâche est redémarrée lorsque l’ordinateur entre dans une condition d’inactivité plusieurs fois.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- Élément RestartOnIdle Planificateur de tâches
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec1d20798b7ceb6ad6ebe2c3a92896600e36eec1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543059"
---
# <a name="restartonidle-idlesettingstype-element"></a>Élément RestartOnIdle (idleSettingsType)

Spécifie si la tâche est redémarrée lorsque l’ordinateur entre dans une condition d’inactivité plusieurs fois.

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

L’élément **RestartOnIdle** est défini par le type complexe [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                       | Dérivé de                                                                 | Description                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est dans un état d’inactivité.<br/> |



## <a name="remarks"></a>Notes

Cet élément est utilisé uniquement si l’élément [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) est défini sur true.

Pour le développement de scripts, ce paramètre de tâche est spécifié à l’aide de la propriété [**IdleSettings. RestartOnIdle**](idlesettings-restartonidle.md) .

Pour le développement C++, ce paramètre de tâche est spécifié à l’aide de la propriété [**IIdleSettings :: RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un paramètre inactif qui indique que la tâche ne doit pas être redémarrée quand la condition d’inactivité est en cycle.


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





