---
title: Type simple CSymbolType (Journal des événements Windows)
description: Définit un nom de symbole C/C++ valide.
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
ms.openlocfilehash: 67b0ccb7c573aa4d71c038f9133cea7c95cdfbd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106539010"
---
# <a name="csymboltype-simple-type-windows-event-log"></a>Type simple CSymbolType (Journal des événements Windows)

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

Si le nom du symbole est vide, le compilateur de message utilise l’attribut **Name** de l’élément que vous définissez pour générer le nom du symbole. Le compilateur remplace tous les caractères non alphanumériques par des traits de soulignement. Par exemple, si l’attribut **Name** du canal est Microsoft-Windows-SampleProvider/Operational, le compilateur utilise Microsoft \_ Windows \_ SampleProvider \_ Operational comme nom de symbole.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



 

 





