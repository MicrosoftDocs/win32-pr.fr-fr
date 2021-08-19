---
description: Type simple CSymbolType (compteurs de performances)-définit un nom de symbole C/C++ valide.
ms.assetid: 75f74a16-0be4-466b-a88d-247c8c94f4ce
title: Type simple CSymbolType (compteurs de performance)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4ebba4d72b7bc79f2aaefccfa2d71e57abd82aa06efb09abc2e83cebdb513f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033529"
---
# <a name="csymboltype-simple-type-performance-counters"></a>Type simple CSymbolType (compteurs de performance)

Définit un nom de symbole C/C++ valide.

``` syntax
<xs:simpleType name="CSymbolType">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="()|([_a-zA-Z][_0-9a-zA-Z]*)"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **CSymbolType** est un **XS : String** qui est limité par le modèle suivant :

-   `()|([_a-zA-Z][_0-9a-zA-Z]*)`

    Le nom du symbole peut être vide ou contenir des caractères alphanumériques et des traits de soulignement. Si vous spécifiez un nom, le nom doit commencer par un trait de soulignement ( \_ ) ou par un caractère alphabétique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




