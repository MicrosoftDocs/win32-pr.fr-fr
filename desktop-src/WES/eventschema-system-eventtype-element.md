---
title: Élément System (EventType)
description: Contient des informations qui identifient le fournisseur et comment il a été activé, l’événement, le canal vers lequel l’événement a été écrit et des informations système telles que les ID de processus et de thread.
ms.assetid: c532cfa3-b722-4227-a403-5c050d62a92c
keywords:
- EventLog, élément du système
topic_type:
- apiref
api_name:
- System
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85f20b364998fb34f3fe9eb6973770b414de501b60e34df6f97a607acb494947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588181"
---
# <a name="system-eventtype-element"></a>Élément System (EventType)

Contient des informations qui identifient le fournisseur et comment il a été activé, l’événement, le canal vers lequel l’événement a été écrit et des informations système telles que les ID de processus et de thread.

``` syntax
<xs:element name="System"
    type="SystemPropertiesType"
 />
```

L’élément **système** est défini par le type complexe [**eventType**](eventschema-eventtype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**événement**](eventschema-event-element.md)
</dt> </dl>

 

 





