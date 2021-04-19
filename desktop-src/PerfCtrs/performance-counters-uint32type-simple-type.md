---
description: Définit un type d’entier non signé.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Type simple UInt32Type (compteurs de performance)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c32901167bcf181e5400ddb1d3b91ed7383965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518681"
---
# <a name="uint32type-simple-type-performance-counters"></a>Type simple UInt32Type (compteurs de performance)

Définit un type d’entier non signé.

``` syntax
<xs:simpleType name="UInt32Type">
    <xs:union
        memberValues="xs:unsignedInt man:HexInt32Type"
     />
</xs:simpleType>
```

## <a name="remarks"></a>Notes

Vous pouvez spécifier la valeur sous la forme d’un entier de 4 octets ou d’une valeur hexadécimale dans la plage comprise entre 0 et 4 294 967 295.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 




