---
title: Élément Provider (SystemPropertiesType)
description: Identifie le fournisseur qui a consigné l’événement.
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- EventLog, élément EventLog
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5327bc267272942df30044678a96244d957122c9fbf7878a805bfd48433e20c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904522"
---
# <a name="provider-systempropertiestype-element"></a>Élément Provider (SystemPropertiesType)

Identifie le fournisseur qui a consigné l’événement.

``` syntax
<xs:element name="Provider">
    <xs:complexType>
        <xs:attribute name="Name"
            type="anyURI"
            use="optional"
         />
        <xs:attribute name="Guid"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="EventSourceName"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

L’élément **Provider** est défini par le type complexe [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Attributs



| Nom            | Type                                                | Description                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| EventSourceName | string                                              | Nom de la source d’événements qui a publié l’événement (si la source de l’événement provient de l’API de [journalisation des événements](/windows/desktop/EventLog/event-logging) héritée).<br/> |
| Guid            | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificateur global unique qui identifie le fournisseur de manière unique.<br/>                                                                   |
| Nom            | anyURI                                              | Nom du fournisseur d’événements qui a consigné l’événement.<br/>                                                                                   |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**Système (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

