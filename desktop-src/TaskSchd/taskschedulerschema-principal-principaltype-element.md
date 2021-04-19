---
title: Élément principal (principalType)
description: Spécifie les informations d’identification de sécurité pour un principal.
ms.assetid: 4ba65976-98d2-4329-80f0-566fac2e9fda
keywords:
- Planificateur de tâches d’élément principal
topic_type:
- apiref
api_name:
- Principal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41d308af651f1aff0ff402c7070adbe631bff9eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510306"
---
# <a name="principal-principaltype-element"></a>Élément principal (principalType)

Spécifie les informations d’identification de sécurité pour un principal. Ces informations d’identification définissent le contexte de sécurité sous lequel une tâche s’exécute.

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

L’élément **principal** est défini par le type complexe [**principalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                               | Dérivé de                                                             | Description                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Principaux**](taskschedulerschema-principals-tasktype-element.md) | [**principalsType**](taskschedulerschema-principalstype-complextype.md) | Spécifie les principaux de sécurité associés à la tâche.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                      | Type                                                          | Description                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**NomComplet**](taskschedulerschema-displayname-principaltype-element.md) | **string**                                                    | Spécifie le nom du principal qui est affiché dans l’interface utilisateur Planificateur de tâches.<br/>                 |
| [**GroupId**](taskschedulerschema-groupid-principaltype-element.md)         | **string**                                                    | Spécifie l’identificateur du groupe d’utilisateurs requis pour exécuter les tâches associées au principal.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)     | [**logonType**](taskschedulerschema-logontype-simpletype.md) | Spécifie la méthode d’ouverture de session de sécurité requise pour exécuter les tâches associées au principal.<br/>  |
| [**IDutilisateur**](taskschedulerschema-userid-principaltype-element.md)           | **string**                                                    | Spécifie l’identificateur d’utilisateur requis pour exécuter les tâches associées au principal.<br/>              |



## <a name="attributes"></a>Attributs



| Nom | Type | Description                                        |
|------|------|----------------------------------------------------|
| Id   | id   | Identificateur de la définition du principal.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de scripts, les informations d’identification de sécurité pour un principal sont spécifiées à l’aide de l’objet [**principal**](principal.md) .

Pour le développement C++, les informations d’identification de sécurité d’un principal sont spécifiées à l’aide de l’interface [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) .

Les éléments enfants répertoriés ci-dessus sont définis par le type complexe [**principalType**](taskschedulerschema-principaltype-complextype.md) . Pour plus d’informations sur le séquencement de ces éléments enfants, consultez [**principalType**](taskschedulerschema-principaltype-complextype.md).

## <a name="examples"></a>Exemples

Le code XML suivant définit un principal avec un identificateur d’utilisateur.


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



Le code XML suivant définit un principal avec un identificateur de groupe.


```XML
<Principals>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
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

 

 





