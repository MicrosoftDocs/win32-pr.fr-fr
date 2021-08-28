---
title: Élément RestartOnFailure (settingsType)
description: Spécifie que l’Planificateur de tâches tentera de redémarrer la tâche si elle échoue pour une raison quelconque.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- Élément RestartOnFailure Planificateur de tâches
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bfe29be7dd329def41e8a6726f141a850eb2daecd05e05d6b5988f543f64864c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072439"
---
# <a name="restartonfailure-settingstype-element"></a>Élément RestartOnFailure (settingsType)

Spécifie que l’Planificateur de tâches tentera de redémarrer la tâche si elle échoue pour une raison quelconque.

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

L’élément **RestartOnFailure** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                              | Type         | Description                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [**Count**](taskschedulerschema-count-restarttype-element.md)       | unsignedByte | Spécifie le nombre de tentatives de redémarrage de la tâche par le Planificateur de tâches.<br/> |
| [**Intervalle**](taskschedulerschema-interval-restarttype-element.md) | duration     | Spécifie la durée pendant laquelle le Planificateur de tâches tente de redémarrer la tâche.<br/>                 |



## <a name="remarks"></a>Remarques

Lorsqu’une application spécifie des paramètres de tâche, ces informations sont accessibles via les propriétés [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) et [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) de l’interface [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) . Pour les scripts, ces informations sont accessibles via les propriétés [**TaskSettings. RestartCount**](tasksettings-restartcount.md) et [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md) .

Les deux éléments enfants doivent être définis pour spécifier la façon dont le Planificateur de tâches redémarre la tâche.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





