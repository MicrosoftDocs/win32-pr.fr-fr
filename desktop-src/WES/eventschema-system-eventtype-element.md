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
ms.openlocfilehash: 4fef0f9f9e24a855564a8d3df2f94610ff9a8248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512356"
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



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Élément parent**
</dt> <dt>

[**événement**](eventschema-event-element.md)
</dt> </dl>

 

 





