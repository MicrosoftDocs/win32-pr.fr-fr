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
ms.openlocfilehash: 0771bb1dffc006abf8e02e6c391278f7d0b03f11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084227"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 




