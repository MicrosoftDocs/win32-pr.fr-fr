---
title: Type Simple CSymbolType (journal des événements Windows)
description: Type Simple CSymbolType (Windows journal des événements)-définit un nom de symbole C/C++ valide.
ms.assetid: d19827b6-2b61-4d75-ac9d-56a384b0cc4b
keywords:
- Journal des types simples CSymbolType
topic_type:
- apiref
api_name:
- CSymbolType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0c8c17a9f4bb7e86b573d60187ffffd55c6cb96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919571"
---
# <a name="csymboltype-simple-type-windows-event-log"></a>Type Simple CSymbolType (journal des événements Windows)

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

    Le nom du symbole peut être vide ou contenir des caractères alphanumériques et des traits de soulignement. Si le nom est vide, le compilateur de message génère le nom du symbole. Si vous spécifiez un nom, le nom doit commencer par un trait de soulignement ( \_ ) ou par un caractère alphabétique.

## <a name="remarks"></a>Notes

Si le nom du symbole est vide, le compilateur de message utilise l’attribut **Name** de l’élément que vous définissez pour générer le nom du symbole. Le compilateur remplace tous les caractères non alphanumériques par des traits de soulignement. par exemple, si l’attribut **name** du canal est microsoft-Windows-SampleProvider/operational, le compilateur utilise microsoft \_ Windows \_ SampleProvider \_ operational comme nom de symbole.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



 

 





