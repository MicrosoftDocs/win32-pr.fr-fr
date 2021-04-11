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
ms.openlocfilehash: c3dc6ae072ed6491915067bea4395a1a84369b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032513"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**Système (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

