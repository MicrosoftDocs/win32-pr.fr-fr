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
ms.openlocfilehash: b793193d7afdfde5fd515252a024432ed45ff8b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105796"
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



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**Système (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





