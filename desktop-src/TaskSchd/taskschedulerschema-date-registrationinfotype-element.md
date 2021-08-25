---
title: Élément Date (registrationInfoType)
description: Spécifie la date et l’heure d’enregistrement de la tâche.
ms.assetid: 0b226786-152d-4231-afa6-db5a630525f3
keywords:
- Élément Date Planificateur de tâches
topic_type:
- apiref
api_name:
- Date
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f191d6181e450deff8ffdb7bda0bf97cd0b27901fe454c25599d17b8edb30628
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866639"
---
# <a name="date-registrationinfotype-element"></a>Élément Date (registrationInfoType)

Spécifie la date et l’heure d’enregistrement de la tâche.

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

L’élément **Date** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                           | Dérivé de                                                                         | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement de script, la date d’inscription d’une tâche est spécifiée à l’aide de la propriété [**RegistrationInfo. date**](registrationinfo-date.md) .

Pour le développement C++, la date d’inscription d’une tâche est spécifiée à l’aide de la propriété [**IRegistrationInfo ::D ATE**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) .

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

 

 





