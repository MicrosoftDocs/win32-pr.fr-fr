---
title: Type simple UInt64Type (schéma EventManifest)
description: Définit un type long non signé.
ms.assetid: 6f69dbde-8292-4f8e-bf49-3ef41ea7315e
keywords:
- Journal des types simples UInt64Type
topic_type:
- apiref
api_name:
- UInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b375a8e452760f9e59bae9cae8449889483d9b4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032814"
---
# <a name="uint64type-simple-type"></a>Type simple UInt64Type

Définit un type long non signé. La valeur peut être spécifiée sous la forme d’un entier de 8 octets ou d’une valeur hexadécimale dans la plage comprise entre 0 et 18446744073709551615.

``` syntax
<xs:simpleType name="UInt64Type">
    <xs:union
        memberValues="unsignedLong HexInt64Type"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





