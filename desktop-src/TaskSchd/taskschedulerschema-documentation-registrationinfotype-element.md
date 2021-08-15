---
title: Élément documentation (registrationInfoType)
description: Spécifie toute documentation supplémentaire pour la tâche.
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- Planificateur de tâches d’élément de documentation
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6cb8c2a78450fffa467ea659b55015f064310783ae21b067093de9473612fcc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356867"
---
# <a name="documentation-registrationinfotype-element"></a>Élément documentation (registrationInfoType)

Spécifie toute documentation supplémentaire pour la tâche.

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

L’élément **documentation** est défini par le type complexe [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                           | Dérivé de                                                                         | Description                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Spécifie les informations d’administration relatives à la tâche, telles que l’auteur de la tâche et la date à laquelle la tâche est inscrite.<br/> |



## <a name="remarks"></a>Remarques

Pour les applications de script, une documentation supplémentaire sur les tâches est spécifiée à l’aide de la propriété [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) .

Pour les applications C++, une documentation supplémentaire sur les tâches est spécifiée à l’aide de la propriété [**IRegistrationInfo ::D ocumentation**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





