---
title: Élément Security (SystemPropertiesType)
description: Identifie l’utilisateur qui a enregistré l’événement.
ms.assetid: f421b0c3-96ea-440c-a3b2-0ddd8f327eec
keywords:
- EventLog, élément de sécurité
topic_type:
- apiref
api_name:
- Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20aef5465b8790bdba92c50181c0550ca5989c29d66fd53b9ec7ed0f760a2129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588285"
---
# <a name="security-systempropertiestype-element"></a>Élément Security (SystemPropertiesType)

Identifie l’utilisateur qui a enregistré l’événement.

``` syntax
<xs:element name="Security">
    <xs:complexType>
        <xs:attribute name="UserID"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

L’élément de **sécurité** est défini par le type complexe [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Attributs



| Nom   | Type   | Description                                                          |
|--------|--------|----------------------------------------------------------------------|
| UserID | string | Identificateur de sécurité (SID) de l’utilisateur sous forme de chaîne.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**Système (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





