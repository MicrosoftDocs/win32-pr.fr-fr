---
title: Élément Hidden (settingsType)
description: Spécifie que la tâche ne sera pas visible dans l’interface utilisateur par défaut.
ms.assetid: a08c270f-6d4e-4473-9538-c1e1e21b3b10
keywords:
- Élément masqué Planificateur de tâches
topic_type:
- apiref
api_name:
- Hidden
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef5ad479fe3107ed8fa79f0f86307254a9f33c4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510579"
---
# <a name="hidden-settingstype-element"></a>Élément Hidden (settingsType)

Spécifie que la tâche ne sera pas visible dans l’interface utilisateur par défaut. Toutefois, les administrateurs peuvent remplacer ce paramètre à l’aide d’un « commutateur maître » qui rend toutes les tâches visibles dans l’interface utilisateur.

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

L’élément **masqué** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété Hidden de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).

Pour le développement de scripts, consultez [**TaskSettings. Hidden**](tasksettings-hidden.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





