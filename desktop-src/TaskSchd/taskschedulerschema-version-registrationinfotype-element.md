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
ms.openlocfilehash: eb1ae5094ad6f69a61e86da1716169a1b7929e3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509300"
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



## <a name="remarks"></a>Notes

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





