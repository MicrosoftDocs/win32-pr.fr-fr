---
title: Élément RequiredPrivileges (requiredPrivilegesType)
description: Spécifie les privilèges requis par la tâche.
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- Élément RequiredPrivileges Planificateur de tâches
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70476cff01113dcf612f890e8a6aa5538d0ca38e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106354"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a>Élément RequiredPrivileges (requiredPrivilegesType)

Spécifie les privilèges requis par la tâche.

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

L’élément **RequiredPrivileges** est défini par le type complexe [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                  | Dérivé de                                                           | Description                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal (principalType)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Spécifie les informations d’identification de sécurité pour un principal.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, ces informations sont accessibles par le biais de la propriété [**IPrincipal2 :: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .

## <a name="examples"></a>Exemples

Le code XML suivant définit l’utilisation d’un identificateur de groupe et des privilèges requis.


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





