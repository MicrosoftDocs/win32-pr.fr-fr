---
title: Élément MultipleInstancesPolicy (settingsType)
description: Spécifie la stratégie qui définit la façon dont le Planificateur de tâches gère plusieurs instances de la tâche.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- Élément MultipleInstancesPolicy Planificateur de tâches
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d7728d2b39fbcbed060fce409f4d721b59ef5ca324cd141d7777a5ffed110a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072449"
---
# <a name="multipleinstancespolicy-settingstype-element"></a>Élément MultipleInstancesPolicy (settingsType)

Spécifie la stratégie qui définit la façon dont le Planificateur de tâches gère plusieurs instances de la tâche.

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

L’élément **MultipleInstancesPolicy** est défini par le type simple [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement C++, consultez la [**propriété MultipleInstances de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).

Pour le développement de scripts, consultez [**TaskSettings. MultipleInstances**](tasksettings-multipleinstances.md).

### <a name="restricted-values"></a>Valeurs restreintes

Cet élément est limité aux valeurs suivantes.

-   Parallel : démarre une nouvelle instance pendant l’exécution d’une instance existante.
-   Queue : démarre une nouvelle instance de la tâche une fois que toutes les autres instances de la tâche sont terminées.
-   IgnoreNew : valeur par défaut. Ne démarre pas une nouvelle instance si une instance existante de la tâche est en cours d’exécution.
-   StopExisting : arrête une instance existante de la tâche avant de démarrer une nouvelle instance.

## <a name="examples"></a>Exemples

Le code XML suivant définit un élément Settings qui permet à plusieurs instances de la tâche de s’exécuter en parallèle.


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
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

 

 





