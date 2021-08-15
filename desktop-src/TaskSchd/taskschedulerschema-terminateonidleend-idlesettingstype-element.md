---
title: Élément StopOnIdleEnd (idleSettingsType)
description: Spécifie que l’Planificateur de tâches arrêtera la tâche si la condition d’inactivité se termine avant la fin de la tâche.
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- Élément StopOnIdleEnd Planificateur de tâches
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e6497ca88d43b96096ee6a23ee81a322b0f397757466ed8cf09dd1b3cd45fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356057"
---
# <a name="stoponidleend-idlesettingstype-element"></a>Élément StopOnIdleEnd (idleSettingsType)

Spécifie que l’Planificateur de tâches arrêtera la tâche si la condition d’inactivité se termine avant la fin de la tâche.

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

L’élément **StopOnIdleEnd** est défini par le type complexe [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                       | Dérivé de                                                                 | Description                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est dans un état d’inactivité.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement C++, consultez la [**propriété StopOnIdleEnd de IIdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).

Pour le développement de scripts, consultez [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md).

## <a name="examples"></a>Exemples

Le code XML suivant définit un paramètre inactif qui indique que la tâche ne doit pas être exécutée lorsque la condition d’inactivité se termine.


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
</IdleSettings>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





