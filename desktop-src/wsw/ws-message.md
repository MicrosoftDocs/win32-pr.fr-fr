---
title: WS_MESSAGE (WebServices. h)
description: Type opaque utilisé pour référencer un objet de message.
ms.assetid: 22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee
keywords:
- WS_MESSAGE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c3581a38e8e8dd93bafeba0375e6b41b14cbdd325ce30bcdc0e110624c6558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026120"
---
# <a name="ws_message"></a>\_message WS

Type opaque utilisé pour référencer un objet de [message](message.md) .


```C++
typedef struct _WS_MESSAGE WS_MESSAGE;
```



## <a name="remarks"></a>Remarques

Cet objet n’est pas thread-safe. Pour plus d’informations, consultez [sécurité des threads](thread-safety.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>WebServices. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Message](message.md)
</dt> <dt>

[Cohérence de thread](thread-safety.md)
</dt> </dl>

 

 





