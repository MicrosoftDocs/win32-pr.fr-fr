---
title: Type complexe BitMapType
description: Définit une liste de mappages nom/valeur entre les valeurs de bits et les valeurs de chaîne.
ms.assetid: 65dc6a48-878c-415c-872c-41dc27691b7f
keywords:
- BitMapType type complexe EventLog
topic_type:
- apiref
api_name:
- BitMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c899718cd28e337bbc5d34301b7bb49446fde51f21db5b742e98dd95c5092c23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590409"
---
# <a name="bitmaptype-complex-type"></a>Type complexe BitMapType

Définit une liste de mappages nom/valeur entre les valeurs de bits et les valeurs de chaîne.

``` syntax
<xs:complexType name="BitMapType">
    <xs:sequence>
        <xs:element name="map"
            type="BitMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                   | Type                                                                       | Description                                                            |
|-----------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**canal**](eventmanifestschema-map-bitmaptype-element.md) | [**BitMapValueType**](eventmanifestschema-bitmapvaluetype-complextype.md) | Définit le mappage entre une valeur de bit et une valeur de chaîne.<br/> |



## <a name="attributes"></a>Attributs



| Nom   | Type                                                              | Description                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | string                                                            | Nom de l'image bitmap.<br/>                                                                                                                                                                                                                                                                                  |
| symbole | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Symbole à utiliser pour référencer les mappages dans votre application. Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le mappage dans le fichier d’en-tête généré par le compilateur. Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





