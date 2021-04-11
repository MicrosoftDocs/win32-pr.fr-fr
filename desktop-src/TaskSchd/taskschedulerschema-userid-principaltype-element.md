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
ms.openlocfilehash: fe12f76c35238251e2ecc60f848e2f7eb4eaa681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385275"
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
| [**Directeur**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Spécifie les informations d’identification de sécurité pour un principal.<br/> |



## <a name="remarks"></a>Notes

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





