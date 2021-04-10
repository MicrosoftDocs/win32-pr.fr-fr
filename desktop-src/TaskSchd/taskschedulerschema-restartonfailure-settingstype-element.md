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
ms.openlocfilehash: 4239d21362d589cae84252c728387b2a2b6159e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200586"
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
| [**Saut**](taskschedulerschema-count-restarttype-element.md)       | unsignedByte | Spécifie le nombre de tentatives de redémarrage de la tâche par le Planificateur de tâches.<br/> |
| [**Défini**](taskschedulerschema-interval-restarttype-element.md) | duration     | Spécifie la durée pendant laquelle le Planificateur de tâches tente de redémarrer la tâche.<br/>                 |



## <a name="remarks"></a>Notes

Lorsqu’une application spécifie des paramètres de tâche, ces informations sont accessibles via les propriétés [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) et [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) de l’interface [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) . Pour les scripts, ces informations sont accessibles via les propriétés [**TaskSettings. RestartCount**](tasksettings-restartcount.md) et [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md) .

Les deux éléments enfants doivent être définis pour spécifier la façon dont le Planificateur de tâches redémarre la tâche.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





