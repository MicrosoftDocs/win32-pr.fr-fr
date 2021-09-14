---
title: Type simple strTableRef
description: Définit une chaîne qui fait référence à une chaîne de message définie dans une table de chaînes du manifeste ou dans un fichier de message (. MC).
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- Journal des types simples strTableRef
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95b7db446af056987e2aa25cd1483e9e53c01d39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192119"
---
# <a name="strtableref-simple-type"></a>Type simple strTableRef

Définit une chaîne qui fait référence à une chaîne de message définie dans une table de chaînes du manifeste ou dans un fichier de message (. MC).

``` syntax
<xs:simpleType name="strTableRef">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **strTableRef** est un **XS : String** qui est limité par le modèle suivant :

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    La chaîne doit se présenter sous la forme $string. *stringid* ou $MC.*symbolid*. Si la chaîne se présente sous la forme, $string. *stringid*, il doit référencer une chaîne dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste. Si la chaîne se présente sous la forme $mc.*symbolid*, elle doit faire référence à un symbole défini dans le fichier de message.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



 

 





