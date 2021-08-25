---
title: Élément UserId (principalType)
description: Spécifie l’identificateur d’utilisateur requis pour exécuter les tâches associées au principal.
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
keywords:
- UserId, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 955dcc93b826b4f86bffd3371ab9907e56dfe7f35649aee603cb18716868f535
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959529"
---
# <a name="userid-principaltype-element"></a>Élément UserId (principalType)

Spécifie l’identificateur d’utilisateur requis pour exécuter les tâches associées au principal.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

L’élément **userid** est défini par le type complexe [**principalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                  | Dérivé de                                                           | Description                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Spécifie les informations d’identification de sécurité pour un principal.<br/> |



## <a name="remarks"></a>Remarques

L’élément **userid** et l’élément [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) sont utilisés ensemble pour définir l’utilisateur requis pour exécuter les tâches qui utilisent ce principal.

Vous ne pouvez pas spécifier d’identificateur d’utilisateur et d’identificateur de groupe en même temps. Spécifiez l' **ID d’utilisateur** ou l’élément [**GroupID**](taskschedulerschema-groupid-principaltype-element.md) , mais pas les deux.

Pour le développement de script, l’identificateur d’utilisateur est spécifié à l’aide de la propriété [**principal. UserID**](principal-userid.md) .

Pour le développement C++, l’identificateur d’utilisateur est spécifié à l’aide de la propriété [**IPrincipal :: userid**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un principe à l’aide d’un identificateur d’utilisateur.


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





