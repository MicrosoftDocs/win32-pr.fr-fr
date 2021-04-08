---
title: Type complexe MapType
description: Définit une liste de paires nom/valeur.
ms.assetid: 208ae219-8f79-4049-b946-a57b33c97b1b
keywords:
- MapType type complexe EventLog
topic_type:
- apiref
api_name:
- MapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4daf6cfe677ab5585ac580e19c868f1bba17de45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740389"
---
# <a name="maptype-complex-type"></a>Type complexe MapType

Définit une liste de paires nom/valeur.

``` syntax
<xs:complexType name="MapType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="valueMap"
            type="ValueMapType"
         />
        <xs:element name="bitMap"
            type="BitMapType"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                          | Type                                                                 | Description                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Pixels**](eventmanifestschema-bitmap-maptype-element.md)     | [**BitMapType**](eventmanifestschema-bitmaptype-complextype.md)     | Définit une liste de paires nom/valeur qui mappent les valeurs de bit et les valeurs de chaîne.<br/>     |
| [**valueMap**](eventmanifestschema-valuemap-maptype-element.md) | [**ValueMapType**](eventmanifestschema-valuemaptype-complextype.md) | Définit une liste de paires nom/valeur qui mappent des valeurs entières et des valeurs de chaîne.<br/> |



## <a name="remarks"></a>Notes

En général, vous créez des mappages pour fournir des valeurs de chaîne énumérées pour les données d’événement.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment spécifier un mappage de valeur et une image bitmap.


```XML
<maps>
   <valueMap name="MyValueMap">
       <map value="5" message="$(string.value5)"/>
       <map value="45" message="$(string.value45)"/>
   </valueMap>
 
   <bitMap name="MyBitmap">
       <map value="0x8" message="$(string.bit3)/>
       <map value="0x80" message="$(string.bit7)/>
   </bitMap>
</maps>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





