---
title: Type complexe InstrumentationType
description: Définit le contenu de la section d’instrumentation du manifeste.
ms.assetid: dbbb978d-50dd-44c0-8bd1-3e48b41afb88
keywords:
- Le type complexe InstrumentationType EventLog
topic_type:
- apiref
api_name:
- InstrumentationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1679ae310a996458aad3e25aba74955036094e00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416295"
---
# <a name="instrumentationtype-complex-type"></a>Type complexe InstrumentationType

Définit le contenu de la section d’instrumentation du manifeste.

``` syntax
<xs:complexType name="InstrumentationType">
    <xs:sequence>
        <xs:element name="events"
            type="EventsType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                  | Type                                                             | Description                                                        |
|--------------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------|
| [**événements**](eventmanifestschema-events-instrumentationtype-element.md) | [**EventsType**](eventmanifestschema-eventstype-complextype.md) | Contient une liste de fournisseurs définie par le manifeste.<br/> |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





