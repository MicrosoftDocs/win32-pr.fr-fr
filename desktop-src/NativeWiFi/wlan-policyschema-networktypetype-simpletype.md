---
description: Définit les types de réseau sans fil.
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: Type simple networkTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 40184bb027f80826baa3ad56090755a2cd9ec630f9eb105e402d30a6ecf2661c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800109"
---
# <a name="networktypetype-simple-type"></a>Type simple networkTypeType

Le type simple networkTypeType définit les types de réseau sans fil. Il existe deux types de réseaux : les réseaux d’infrastructure (ESS) et les réseaux ad hoc (IBSS).

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valeurs d’énumération

Le type simple **networkTypeType** définit les valeurs suivantes.



| Valeur | Description |
|-------|-------------|
| IBSS  |             |
| CCÈS   |             |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




