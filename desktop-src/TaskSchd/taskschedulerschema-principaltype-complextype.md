---
title: Type complexe principalType
description: Définit l’attribut, les éléments enfants et les informations de séquencement pour l’élément principal.
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- Planificateur de tâches de type complexe principalType
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 037013a4b40984df41e52aa13be69c1247b1c05c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466275"
---
# <a name="principaltype-complex-type"></a>Type complexe principalType

Définit l’attribut, les éléments enfants et les informations de séquencement pour l’élément [**principal**](taskschedulerschema-principal-principaltype-element.md) .

``` syntax
<xs:complexType name="principalType">
    <xs:all>
        <xs:element name="UserId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="LogonType"
            type="logonType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="GroupId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="DisplayName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunLevel"
            type="runLevelType"
            minOccurs="0"
         />
        <xs:element name="ProcessTokenSidType"
            type="processTokenSidType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="RequiredPrivileges"
            type="requiredPrivilegesType"
            minOccurs="0"
         />
    </xs:all>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                             | Type                                                                                     | Description                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**NomComplet**](taskschedulerschema-displayname-principaltype-element.md)                        | string                                                                                   | Spécifie le nom du principal qui est affiché dans l’interface utilisateur Planificateur de tâches.<br/>                 |
| [**GroupId**](taskschedulerschema-groupid-principaltype-element.md)                                | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                  | Spécifie l’identificateur du groupe d’utilisateurs requis pour exécuter les tâches associées au principal.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)                            | [**logonType**](taskschedulerschema-logontype-simpletype.md)                            | Spécifie la méthode d’ouverture de session de sécurité requise pour exécuter les tâches associées au principal.<br/>        |
| [**ProcessTokenSidType**](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [**processTokenSidType**](taskschedulerschema-processtokensidtype-simpletype.md)        | Spécifie les types d’identificateur de sécurité (SID) de processus qui peuvent être utilisés par les tâches.<br/>                              |
| [**RequiredPrivileges**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) | Spécifie les privilèges requis pour exécuter la tâche.<br/>                                                               |
| [**RunLevel**](taskschedulerschema-runlevel-principaltype-element.md)                              | [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md)                      | Spécifie le niveau d’autorisation sur lequel la tâche sera exécutée.<br/>                                                     |
| [**IDutilisateur**](taskschedulerschema-userid-principaltype-element.md)                                  | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                  | Spécifie l’identificateur d’utilisateur requis pour exécuter les tâches associées au principal.<br/>              |



## <a name="attributes"></a>Attributs



| Nom | Type | Description                                           |
|------|------|-------------------------------------------------------|
| id   | id   | Spécifie l’identificateur du principal.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types complexes de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





