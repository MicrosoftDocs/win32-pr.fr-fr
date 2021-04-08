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
ms.openlocfilehash: 55b57b63f3e5c9e5a5c4cd15974c89f6d28439f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739732"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





