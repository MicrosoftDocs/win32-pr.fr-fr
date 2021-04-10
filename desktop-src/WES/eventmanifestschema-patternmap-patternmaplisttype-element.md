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
ms.openlocfilehash: 3ae29d60e39515a7c4b4db334f947abc44df5ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032288"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**patternMaps (NamedQueryType)**](eventmanifestschema-patternmaps-namedquerytype-element.md)
</dt> </dl>

 

 





