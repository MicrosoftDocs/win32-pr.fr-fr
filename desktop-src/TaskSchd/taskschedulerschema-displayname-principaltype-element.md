---
title: DisplayName (principalType) (élément)
description: Spécifie le nom du principal qui est affiché dans l’interface utilisateur Planificateur de tâches.
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- DisplayName, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8ef310869ea8558bca231e866ddeefc0dc35944
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857325"
---
# <a name="displayname-principaltype-element"></a>DisplayName (principalType) (élément)

Spécifie le nom du principal qui est affiché dans l’interface utilisateur Planificateur de tâches.

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

L’élément **DisplayName** est défini par le type complexe [**principalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                  | Dérivé de                                                           | Description                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Spécifie les informations d’identification de sécurité pour un principal.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de scripts, le nom complet du principal est spécifié à l’aide de la propriété [**principal. DisplayName**](principal-displayname.md) .

Pour le développement C++, le nom complet du principal est spécifié à l’aide de la propriété [**IPrincipal ::D isplayname**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un à l’aide d’un identificateur de groupe et d’un nom d’affichage.


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



Le code XML suivant définit un principal à l’aide d’un identificateur d’utilisateur et d’un nom d’affichage.


```XML
<Principal>
    <UserId></UserId>
    <LogonType></LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





