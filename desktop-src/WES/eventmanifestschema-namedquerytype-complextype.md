---
title: Type complexe NamedQueryType
description: Non utilisé. Définit une liste de requêtes nommées qui interrogent la chaîne de message d’événement pour obtenir une valeur et effectuent une action spécifiée si elle est trouvée. | Type complexe NamedQueryType
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- NamedQueryType type complexe EventLog
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba83c2716b765082cdd32458a093bc0300fea369a810251e6f5ebf28e97f9485
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652159"
---
# <a name="namedquerytype-complex-type"></a>Type complexe NamedQueryType

Non utilisé. Définit une liste de requêtes nommées qui interrogent la chaîne de message d’événement pour obtenir une valeur et effectuent une action spécifiée si elle est trouvée.

``` syntax
<xs:complexType name="NamedQueryType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="patternMaps"
            type="PatternMapListType"
         />
        <xs:any
            processContents="lax"
            maxOccurs="unbounded"
            minOccurs="0"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                       | Type                                                                             | Description                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**patternMaps**](eventmanifestschema-patternmaps-namedquerytype-element.md) | [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) | Définit une liste de paires d’expressions régulières utilisées pour modifier la chaîne de message.<br/> |



## <a name="examples"></a>Exemples

L’exemple suivant montre comment utiliser l’élément [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) . Cet exemple prend le contenu de la chaîne de message et l’insère dans la chaîne https://www .*MessageString*. com. Il remplace ensuite la chaîne de message par le résultat. Par exemple, si la chaîne de message contient Microsoft, la requête remplacerait la chaîne de message Microsoft par https://www.Microsoft.com .


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





