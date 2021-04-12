---
title: Élément UserId (logonTriggerType)
description: Identificateur de l’utilisateur. La tâche est démarrée lorsque cet utilisateur ouvre une session sur l’ordinateur.
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
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
ms.openlocfilehash: 69d6534122b4b5e11a18a64ffa9bbb5e29e2a68a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519106"
---
# <a name="userid-logontriggertype-element"></a>Élément UserId (logonTriggerType)

Identificateur de l’utilisateur. La tâche est démarrée lorsque cet utilisateur ouvre une session sur l’ordinateur.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

L’élément **userid** est défini par le type complexe [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                       | Dérivé de                                                                 | Description                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) | [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) | Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de script, l’identificateur d’utilisateur du déclencheur LOGON est spécifié à l’aide de la propriété [**LogonTrigger. UserID**](logontrigger-userid.md) .

Pour le développement C++, l’identificateur d’utilisateur du déclencheur LOGON est spécifié à l’aide de la propriété [**ILogonTrigger :: userid**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui spécifie un déclencheur LOGON, consultez [exemple de déclencheur de connexion (XML)](logon-trigger-example--xml-.md).

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

 

 





