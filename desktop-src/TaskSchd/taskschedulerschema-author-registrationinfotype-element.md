---
title: Élément Author (registrationInfoType)
description: Spécifie l’auteur de la tâche.
ms.assetid: 1faa4952-0737-4313-afa5-4a9bad5daaff
keywords:
- Élément author Planificateur de tâches
topic_type:
- apiref
api_name:
- Author
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d368093a266827004cddf23dc7ba5d82f108f99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942346"
---
# <a name="author-registrationinfotype-element"></a>Élément Author (registrationInfoType)

Spécifie l’auteur de la tâche.

``` syntax
<xs:element name="Author"
    type="string"
    minOccurs="0"
 />
```

L’élément **Author** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                           | Dérivé de                                                                         | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de script, l’auteur de la tâche est spécifié à l’aide de la propriété [**RegistrationInfo. Author**](registrationinfo-author.md) .

Pour le développement C++, l’auteur de la tâche est spécifié à l’aide de la propriété [**IRegistrationInfo :: Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) .

## <a name="examples"></a>Exemples

Le code XML suivant définit l’auteur d’une tâche.


```XML
<RegistrationInfo>
    <Author></Author>
 </RegistrationInfo>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





