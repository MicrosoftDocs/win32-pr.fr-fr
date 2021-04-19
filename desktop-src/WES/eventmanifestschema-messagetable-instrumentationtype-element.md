---
title: Élément messageTable (EventsType)
description: Contient une référence à une chaîne dans la section localisation du manifeste. | Élément messageTable (EventsType)
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
keywords:
- EventLog, élément messageTable
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85ce478fb30389ba911ef9dd76473a6261974f55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106537203"
---
# <a name="messagetable-eventstype-element"></a>Élément messageTable (EventsType)

Contient une référence à une chaîne dans la section localisation du manifeste.

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L’élément **messageTable** est défini par le type complexe [**EventsType**](eventmanifestschema-eventstype-complextype.md) .

## <a name="child-elements"></a>Éléments enfants



| Élément                                                             | Type | Description                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [**Message**](eventmanifestschema-message-messagetable-element.md) |      | Spécifie une référence à une chaîne dans la section localisation du manifeste.<br/> |



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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Éléments parents**
</dt> <dt>

[**Élément Events (InstrumentationType)**](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





