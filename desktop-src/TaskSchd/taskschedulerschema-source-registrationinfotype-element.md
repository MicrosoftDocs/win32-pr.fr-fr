---
title: Élément source (registrationInfoType)
description: Spécifie l’origine de la tâche. Par exemple, à partir d’un composant, d’un service, d’une application ou d’un utilisateur.
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- Planificateur de tâches de l’élément source
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: faf5532909e8f692aa2c438186a17cf9669170bb4a7d9666682d07ba8d4ea583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139162"
---
# <a name="source-registrationinfotype-element"></a>Élément source (registrationInfoType)

Spécifie l’origine de la tâche. Par exemple, à partir d’un composant, d’un service, d’une application ou d’un utilisateur.

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

L’élément **source** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                           | Dérivé de                                                                         | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement de script, la source d’une tâche est spécifiée à l’aide de la propriété [**RegistrationInfo. source**](registrationinfo-source.md) .

Pour le développement C++, la source d’une tâche est spécifiée à l’aide de la propriété [**IRegistrationInfo :: source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) .

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

 

 





