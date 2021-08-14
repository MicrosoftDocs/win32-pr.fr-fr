---
title: Type simple versionType
description: Définit un modèle qui spécifie une version d’une tâche.
ms.assetid: e9eebbc1-5465-4af6-8b97-f1fd5827442e
keywords:
- Planificateur de tâches de type simple versionType
topic_type:
- apiref
api_name:
- versionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 52ad30f5ea14a447e2a08151ef2803b0577066e147e29673d373ce87eee033f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355035"
---
# <a name="versiontype-simple-type"></a>Type simple versionType

Définit un modèle qui spécifie une version d’une tâche.

``` syntax
<xs:simpleType name="versionType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\d+(\.\d+){1,3}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **versionType** est une **chaîne** qui est limitée par le modèle suivant :

-   `\d+(\.\d+){1,3}`

    Double suivi d’un, deux ou trois doubles. Par exemple, 1,2 ou 1.2.3.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





