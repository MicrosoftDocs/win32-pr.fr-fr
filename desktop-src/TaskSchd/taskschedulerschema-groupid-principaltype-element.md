---
title: Élément GroupId (principalType)
description: Spécifie l’identificateur du groupe d’utilisateurs requis pour exécuter les tâches associées au principal.
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- Élément GroupId Planificateur de tâches
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4376e7037c228ebf2d2ffdc193cc34e7f92647220251cd82f09b0b65c7f9a81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131838"
---
# <a name="groupid-principaltype-element"></a>Élément GroupId (principalType)

Spécifie l’identificateur du groupe d’utilisateurs requis pour exécuter les tâches associées au principal.

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

L’élément **GroupID** est défini par le type complexe [**principalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                  | Dérivé de                                                           | Description                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Spécifie les informations d’identification de sécurité pour un principal.<br/> |



## <a name="remarks"></a>Remarques

Vous ne pouvez pas spécifier un identificateur de groupe et un identificateur d’utilisateur en même temps. Spécifiez les éléments [**userid**](taskschedulerschema-userid-principaltype-element.md) ou **GroupID** , mais pas les deux.

Pour le développement de script, l’identificateur de groupe du principal est spécifié à l’aide de la propriété [**principal. GroupId**](principal-groupid.md) .

Pour le développement C++, l’identificateur de groupe du principal est spécifié à l’aide de la propriété [**IPrincipal :: GroupID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui utilise cet élément, consultez [exemple de déclencheur de connexion (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





