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
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218329"
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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




