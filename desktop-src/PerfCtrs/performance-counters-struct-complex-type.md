---
description: Définit une structure qui contient une ou plusieurs valeurs de compteur.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: Type complexe struct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29796a259810cd03739c45338709966bd765f0c1fd9026777f435acb2c5de253
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978849"
---
# <a name="struct-complex-type"></a>Type complexe struct

Définit une structure qui contient une ou plusieurs valeurs de compteur.

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributs



| Nom | Type                                                                    | Description                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| name | [**homme : CSymbolType**](performance-counters-csymboltype-simple-type.md) | Nom de la structure.<br/>                                                                                                            |
| type | [**homme : CSymbolType**](performance-counters-csymboltype-simple-type.md) | Nom symbolique qui identifie la structure. L’outil [CTRPP](ctrpp.md) crée une variable de struct portant ce nom que vous pouvez utiliser.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




