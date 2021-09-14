---
title: WS_MESSAGE (WebServices. h)
description: Type opaque utilisé pour référencer un objet de message.
ms.assetid: 22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee
keywords:
- WS_MESSAGE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa9230648adfc6da3bab954a91d04d2e9991a8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219305"
---
# <a name="ws_message"></a>\_message WS

Type opaque utilisé pour référencer un objet de [message](message.md) .


```C++
typedef struct _WS_MESSAGE WS_MESSAGE;
```



## <a name="remarks"></a>Notes

Cet objet n’est pas thread-safe. Pour plus d’informations, consultez [sécurité des threads](thread-safety.md).

## <a name="requirements"></a>Spécifications



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

 

 





