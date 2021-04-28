---
description: Type simple UInt32Type (compteurs de performance)-définit un type entier non signé.
ms.assetid: 48df484d-d663-42fa-aaec-51c463bb5350
title: Type simple UInt32Type (compteurs de performance)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32f8a4bbf00f569ba98dfc031f62717b1afc8734
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114577"
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



 

 




