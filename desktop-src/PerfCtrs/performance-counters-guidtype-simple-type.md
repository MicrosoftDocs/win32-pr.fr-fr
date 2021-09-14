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
ms.openlocfilehash: 758509a564c26db493fa2e9ed971aba71878cdbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218404"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




