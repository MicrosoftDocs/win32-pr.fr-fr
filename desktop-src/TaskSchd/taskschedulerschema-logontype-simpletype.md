---
title: Type simple logonType
description: Définit les valeurs possibles de l’élément LogonType.
ms.assetid: a08cd549-f45c-4278-a428-1ffe91b67564
keywords:
- Planificateur de tâches de type simple logonType
topic_type:
- apiref
api_name:
- logonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58d8c859502e81b5c5101adac3c8c26539870dd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105214"
---
# <a name="logontype-simple-type"></a>Type simple logonType

Définit les valeurs possibles de l’élément [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .

``` syntax
<xs:simpleType name="logonType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="S4U"
         />
        <xs:enumeration
            value="Password"
         />
        <xs:enumeration
            value="InteractiveToken"
         />
        <xs:enumeration
            value="InteractiveTokenOrPassword"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valeurs d’énumération

Le type simple **LogonType** définit les valeurs suivantes.



| Valeur                      | Description                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S4U                        | L’utilisateur doit se connecter à l’aide d’une connexion S4U (service for user). Lorsqu’une ouverture de session S4U est utilisée, aucun mot de passe n’est stocké par le système et il n’y a aucun accès au réseau ou aux fichiers chiffrés.<br/>                                                                                                                                                          |
| Mot de passe                   | L’utilisateur doit se connecter à l’aide d’un mot de passe.<br/>                                                                                                                                                                                                                                                                                                              |
| InteractiveToken           | L’utilisateur doit déjà avoir ouvert une session. La tâche est exécutée uniquement dans une session interactive existante.<br/>                                                                                                                                                                                                                                                   |
| InteractiveTokenOrPassword | N’est plus utilisé ; actuellement identique au mot de passe.<br/> **Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows Vista et Windows server 2008 :** La tâche est exécutée dans une session interactive existante ou l’utilisateur doit ouvrir une session à l’aide d’un mot de passe.<br/> <br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types simples de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





