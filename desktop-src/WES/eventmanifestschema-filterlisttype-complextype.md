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
ms.openlocfilehash: d1071fbbb9eba6bf6ebf0d74d4caaac50e1ccce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317462"
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



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



 

