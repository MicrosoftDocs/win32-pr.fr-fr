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
ms.openlocfilehash: a47a01d7d77f3dd20f055bce8e4bb12fad82c771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942729"
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



## <a name="remarks"></a>Notes

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





