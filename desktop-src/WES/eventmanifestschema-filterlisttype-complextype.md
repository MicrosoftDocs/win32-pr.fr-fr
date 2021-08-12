---
title: Type complexe FilterListType
description: Définit une liste de filtres qu’un contrôleur ETW peut passer à votre fournisseur pour limiter davantage les événements qu’il écrit.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- FilterListType type complexe EventLog
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b66ccc002372159540895dfbe95786921266320bb4d3a4e6827085ae7822c12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589624"
---
# <a name="filterlisttype-complex-type"></a>Type complexe FilterListType

Définit une liste de filtres qu’un contrôleur ETW peut passer à votre fournisseur pour limiter davantage les événements qu’il écrit.

``` syntax
<xs:complexType name="FilterListType">
    <xs:sequence>
        <xs:element name="filter"
            type="FilterType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément    | Type                                                             | Description                   |
|------------|------------------------------------------------------------------|-------------------------------|
| **filter** | [**FilterType**](eventmanifestschema-filtertype-complextype.md) | Liste de filtres.<br/> |



## <a name="remarks"></a>Notes

Un contrôleur ETW est une application qui appelle la fonction [**StartTrace**](/windows/desktop/ETW/starttrace) pour créer une session ETW. Pour plus d’informations, consultez [contrôle des sessions de suivi d’événements](/windows/desktop/ETW/controlling-event-tracing-sessions). Le contrôleur peut utiliser la fonction [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) pour énumérer les filtres que vous définissez. Le contrôleur peut alors passer un ou plusieurs filtres lorsqu’il appelle la fonction [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) pour activer votre fournisseur. Votre fournisseur reçoit les filtres, ainsi que le reste des paramètres Enable, dans votre fonction de rappel [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



 

