---
title: Élément Data (taskType)
description: Définit des données supplémentaires associées à la tâche, mais qui, sinon, ne sont pas utilisées par le service Planificateur de tâches.
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
keywords:
- Planificateur de tâches d’élément de données
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3afff1cbd81ede49568afdc9e516d87a57ff9e5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011040"
---
# <a name="data-tasktype-element"></a>Élément Data (taskType)

Définit des données supplémentaires associées à la tâche, mais qui, sinon, ne sont pas utilisées par le service Planificateur de tâches.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

L’élément de **données** est défini par le type complexe [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                          | Dérivé de                                                 | Description                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Tâche**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Définit la tâche qui est effectuée par le service Planificateur de tâches.<br/> |



## <a name="remarks"></a>Notes

En guise d’exemple de ce type de données, le service de Journaux et alertes de performance utilise cette propriété comme un conteneur de stockage pour la requête de compteur de performances associée à une tâche.

Pour le développement C++, les données d’une tâche sont spécifiées à l’aide [**de la propriété de données de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).

Dans le développement de scripts, les données d’une tâche sont spécifiées à l’aide de la propriété [**TaskDefinition. Data**](taskdefinition-data.md) .

## <a name="requirements"></a>Spécifications



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

 

 





