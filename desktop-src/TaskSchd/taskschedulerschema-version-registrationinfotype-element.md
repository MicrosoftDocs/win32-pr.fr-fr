---
title: Élément version (registrationInfoType)
description: Spécifie le numéro de version de la tâche.
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- Version, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63d69b501b12890939f3bd0b146c959278eeaa0d5eb596851a488cef87f0770a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610424"
---
# <a name="version-registrationinfotype-element"></a>Élément version (registrationInfoType)

Spécifie le numéro de version de la tâche.

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

L’élément **version** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                           | Dérivé de                                                                         | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement de script, la version d’une tâche est spécifiée à l’aide de la propriété [**RegistrationInfo. version**](registrationinfo-version.md) .

Pour le développement C++, la version d’une tâche est spécifiée à l’aide de la propriété [**IRegistrationInfo :: version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) .

## <a name="examples"></a>Exemples

Le code XML suivant définit la version d’une tâche.


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



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

 

 





