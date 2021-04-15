---
title: Type complexe PatternMapType
description: Non utilisé. Définit un mappage entre deux expressions régulières. Une expression est utilisée pour rechercher une chaîne correspondante dans la chaîne de message, tandis que l’autre est utilisée pour modifier la chaîne avant que le service la replace dans la chaîne de message.
ms.assetid: 184b6aeb-a554-4a92-b19e-1849c711d33b
keywords:
- PatternMapType type complexe EventLog
topic_type:
- apiref
api_name:
- PatternMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e39ca30520f4f595bfc73a4d80b9bc191793859a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465758"
---
# <a name="patternmaptype-complex-type"></a>Type complexe PatternMapType

Non utilisé. Définit un mappage entre deux expressions régulières. Une expression est utilisée pour rechercher une chaîne correspondante dans la chaîne de message, tandis que l’autre est utilisée pour modifier la chaîne avant que le service la replace dans la chaîne de message.

``` syntax
<xs:complexType name="PatternMapType">
    <xs:sequence>
        <xs:element name="map"
            type="PatternMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="format"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                       | Type                                                                               | Description                                                                                                   |
|---------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**canal**](eventmanifestschema-map-patternmaptype-element.md) | [**PatternMapValueType**](eventmanifestschema-patternmapvaluetype-complextype.md) | Définit les expressions régulières utilisées pour rechercher une chaîne correspondante dans la chaîne de message et la modifier.<br/> |



## <a name="attributes"></a>Attributs



| Nom   | Type                                                              | Description                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| format | anyURI                                                            | Moteur d’expression régulière à utiliser.<br/>                                                                                                                                                                                                                                                                    |
| name   | **QName**                                                         | Nom de la carte de modèle. Utilisez le nom dans un élément de données pour référencer les mappages.<br/>                                                                                                                                                                                                                   |
| symbole | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Symbole à utiliser pour référencer les mappages dans votre application. Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le mappage dans le fichier d’en-tête généré par le compilateur. Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





