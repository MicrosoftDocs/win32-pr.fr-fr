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
ms.openlocfilehash: ef3a48b102b9ab36ef492fcd38c4bb8b2560d5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466974"
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



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





