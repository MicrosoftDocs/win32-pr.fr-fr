---
title: Type complexe PatternMapValueType
description: Non utilisé. Définit les expressions régulières utilisées pour rechercher une chaîne correspondante dans la chaîne de message et la modifier.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- PatternMapValueType type complexe EventLog
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc36564aefd4d2f3d19f3b216d785faad888612621386037ae0e5539ce511169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136162"
---
# <a name="patternmapvaluetype-complex-type"></a>Type complexe PatternMapValueType

Non utilisé. Définit les expressions régulières utilisées pour rechercher une chaîne correspondante dans la chaîne de message et la modifier.

``` syntax
<xs:complexType name="PatternMapValueType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="value"
                type="string"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributs



| Nom  | Type   | Description                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| name  | string | Expression régulière utilisée pour rechercher une chaîne correspondante dans la chaîne de message.<br/>                   |
| value | string | Expression régulière utilisée pour modifier la chaîne correspondante trouvée dans la chaîne de message.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





