---
title: Description (registrationInfoType) (élément)
description: Spécifie la description de la tâche.
ms.assetid: bf3552eb-01a6-4651-ae43-4b4e8eef3faf
keywords:
- Élément Description Planificateur de tâches
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a6fef3012913eacfb8b8aa111793bd77255512d551bea0ab123d45b9caed6501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991389"
---
# <a name="description-registrationinfotype-element"></a>Description (registrationInfoType) (élément)

Spécifie la description de la tâche.

``` syntax
<xs:element name="Description"
    type="string"
    minOccurs="0"
 />
```

L’élément **Description** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                           | Dérivé de                                                                         | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement de script, la description d’une tâche est spécifiée à l’aide de la propriété [**RegistrationInfo. Description**](registrationinfo-description.md) .

Pour le développement C++, la description d’une tâche est spécifiée à l’aide de la propriété [**IRegistrationInfo ::D escription**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) .

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

 

 





