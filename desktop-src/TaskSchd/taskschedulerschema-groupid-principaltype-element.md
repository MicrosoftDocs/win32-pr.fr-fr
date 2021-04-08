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
ms.openlocfilehash: 080a408f65ac7a36ada1751bbd5cb95395cf0b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033123"
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
| [**Directeur**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Spécifie les informations d’identification de sécurité pour un principal.<br/> |



## <a name="remarks"></a>Notes

Vous ne pouvez pas spécifier un identificateur de groupe et un identificateur d’utilisateur en même temps. Spécifiez les éléments [**userid**](taskschedulerschema-userid-principaltype-element.md) ou **GroupID** , mais pas les deux.

Pour le développement de script, l’identificateur de groupe du principal est spécifié à l’aide de la propriété [**principal. GroupId**](principal-groupid.md) .

Pour le développement C++, l’identificateur de groupe du principal est spécifié à l’aide de la propriété [**IPrincipal :: GroupID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui utilise cet élément, consultez [exemple de déclencheur de connexion (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





