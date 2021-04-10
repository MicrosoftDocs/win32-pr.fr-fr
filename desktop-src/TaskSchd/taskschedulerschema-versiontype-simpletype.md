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
ms.openlocfilehash: df7010c6ecba29ad0ade80ce403018dd626d01cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317170"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





