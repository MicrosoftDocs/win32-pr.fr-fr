---
title: Élément ExecutionTimeLimit (settingsType)
description: Durée d’exécution de la tâche.
ms.assetid: c42d0f42-4571-44ab-90b1-948fd7ea991b
keywords:
- Élément ExecutionTimeLimit Planificateur de tâches
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f6519495cc16cdff6a30c65f75468bd676ca1f2750faedb5c632972c1affb996
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356415"
---
# <a name="executiontimelimit-settingstype-element"></a>Élément ExecutionTimeLimit (settingsType)

Durée d’exécution de la tâche. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes). Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> . La valeur PT0S permet à la tâche de s’exécuter indéfiniment.

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
    minOccurs="0"
 />
```

L’élément **ExecutionTimeLimit** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement C++, consultez la [**propriété ExecutionTimeLimit de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).

Pour le développement de scripts, consultez [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





