---
title: Privilege (élément requiredPrivilegesType)
description: Spécifie le droit d’une tâche à effectuer diverses opérations liées au système, telles que l’arrêt du système, le chargement des pilotes de périphérique ou la modification de l’heure système.
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- Privilège, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e9263ae9d02bb384bfbe56101ea82f98c2e076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466422"
---
# <a name="privilege-requiredprivilegestype-element"></a>Privilege (élément requiredPrivilegesType)

Spécifie le droit d’une tâche à effectuer diverses opérations liées au système, telles que l’arrêt du système, le chargement des pilotes de périphérique ou la modification de l’heure système.

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

L’élément **Privilege** est défini par le type complexe [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                             | Dérivé de                                                                             | Description                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**RequiredPrivileges**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, ces informations sont accessibles par le biais de la propriété [**IPrincipal2 :: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un élément Settings qui spécifie le droit d’une tâche à effectuer diverses opérations liées au système, telles que l’arrêt du système, le chargement des pilotes de périphérique ou la modification de l’heure système.


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

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





