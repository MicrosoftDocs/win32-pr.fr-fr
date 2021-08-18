---
description: Définit un type d’identificateur global unique, au format de registre.
ms.assetid: 2be73c57-b6b6-46ab-93e1-d70f8655c30e
title: Type simple GUIDType (compteurs de performance)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 305195784a3578242caefc1fb7eb9bcd8dbd5b557d89d8752bc8242f648abbdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119624919"
---
# <a name="guidtype-simple-type-performance-counters"></a>Type simple GUIDType (compteurs de performance)

Définit un type d’identificateur global unique, au format de registre.

``` syntax
<xs:simpleType name="GUIDType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **GUIDType** est un **XS : String** qui est limité par le modèle suivant :

-   `\{[0-9a-fA-F]{8}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{4}-[0-9a-fA-F]{12}\}`

    La valeur doit être un type d’identificateur global unique au format du Registre. Par exemple, {5b2fc63a-8AF4-44cb-960C-aefdced908d6}. Utilisez GUIDGen.exe ou UUIDGen.exe pour créer un GUID.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




