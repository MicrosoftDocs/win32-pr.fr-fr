---
title: Élément message (messageTable)
description: Contient une référence à une chaîne dans la section localisation du manifeste. | Élément message (messageTable)
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- message, élément EventLog
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79020fa18717a3a2338a8ac243bb95e0fa14de47f0e434fb52c475c956afa101
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865669"
---
# <a name="message-messagetable-element"></a>Élément message (messageTable)

Contient une référence à une chaîne dans la section localisation du manifeste.

``` syntax
<xs:element name="message">
    <xs:complexType>
        <xs:attribute name="value"
            type="string"
            use="required"
         />
        <xs:attribute name="mid"
            type="string"
            use="optional"
         />
        <xs:attribute name="message"
            type="string"
            use="required"
         />
        <xs:attribute name="symbol"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

L’élément **message** est défini par l’élément [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md) .

## <a name="attributes"></a>Attributs



| Nom    | Type   | Description                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| message | string | Référence à la chaîne localisée dans la table de chaînes.<br/>                                |
| mid     | string | Non utilisé.<br/>                                                                               |
| symbole  | string | Nom symbolique que vous souhaitez que le compilateur de message crée pour cette chaîne de message.<br/> |
| value   | string | Nombre à utiliser comme identificateur de message pour ce message.<br/>                           |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Éléments parents**
</dt> <dt>

[**messageTable (EventsType)**](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[**messageTable (type de données)**](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





