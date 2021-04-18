---
title: Élément LogonType (principalType)
description: Spécifie la méthode d’ouverture de session de sécurité requise pour exécuter les tâches associées au principal.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- Élément LogonType Planificateur de tâches
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a382225f526f18731b8b9f0541e617cb31dfb4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512556"
---
# <a name="logontype-principaltype-element"></a>Élément LogonType (principalType)

Spécifie la méthode d’ouverture de session de sécurité requise pour exécuter les tâches associées au principal.

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

L’élément **LogonType** est défini par le type complexe [**principalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                  | Dérivé de                                                           | Description                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Directeur**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Spécifie les informations d’identification de sécurité pour un principal.<br/> |



## <a name="remarks"></a>Notes

L’élément **LogonType** et l’élément [**userid**](taskschedulerschema-userid-principaltype-element.md) sont utilisés ensemble pour définir l’utilisateur requis pour exécuter les tâches qui utilisent ce principal.

Pour le développement de scripts, le type d’ouverture de session du principal est spécifié par la propriété [**principal. LogonType**](principal-logontype.md) .

Pour le développement C++, le type d’ouverture de session du principal est spécifié par la propriété [**IPrincipal :: LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) .

Cet élément (défini par le type simple [**LogonType**](taskschedulerschema-logontype-simpletype.md) ) doit avoir l’une des valeurs suivantes.

-   S4U : l’utilisateur doit se connecter à l’aide d’une connexion S4U (service for user). Lorsqu’une ouverture de session S4U est utilisée, aucun mot de passe n’est stocké par le système et il n’y a pas d’accès au réseau ou aux fichiers chiffrés.
-   Mot de passe : l’utilisateur doit se connecter à l’aide d’un mot de passe.
-   InteractiveToken : l’utilisateur doit déjà avoir ouvert une session. La tâche est exécutée uniquement dans une session interactive existante.

Pour une tâche, qui contient une action de MessageBox, la boîte de message s’affiche si la tâche est activée et que la tâche a un type de connexion interactive. Pour définir le type d’ouverture de session de la tâche sur Interactive, spécifiez **InteractiveToken** dans l' **<LogonType>** élément du principal de tâche.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





