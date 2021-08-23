---
title: Élément patternMap (PatternMapListType)
description: Définit un mappage entre deux expressions régulières. Une expression est utilisée pour rechercher une chaîne correspondante dans la chaîne de message, tandis que l’autre est utilisée pour modifier la chaîne avant que le service la replace dans la chaîne de message.
ms.assetid: 5cf28d38-4cc3-4a7b-a64b-3ad1cb42ebef
keywords:
- EventLog, élément patternMap
topic_type:
- apiref
api_name:
- patternMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9206726bb960762d482c5a966fce6fb5a89b094249f247c2617c051d76d7e7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055967"
---
# <a name="patternmap-patternmaplisttype-element"></a>Élément patternMap (PatternMapListType)

Définit un mappage entre deux expressions régulières. Une expression est utilisée pour rechercher une chaîne correspondante dans la chaîne de message, tandis que l’autre est utilisée pour modifier la chaîne avant que le service la replace dans la chaîne de message.

``` syntax
<xs:element name="patternMap"
    type="PatternMapType"
 />
```

L’élément **patternMap** est défini par le type complexe [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**patternMaps (NamedQueryType)**](eventmanifestschema-patternmaps-namedquerytype-element.md)
</dt> </dl>

 

 





