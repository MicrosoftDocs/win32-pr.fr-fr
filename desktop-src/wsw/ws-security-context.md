---
title: WS_SECURITY_CONTEXT (WebServices. h)
description: Type opaque utilisé pour référencer un objet de contexte de sécurité.
ms.assetid: 8d23357b-bff8-45fe-80ef-df3f3b0edde1
keywords:
- WS_SECURITY_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c041307eadd1ebcea379f9de0880fc011bd137ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234377"
---
# <a name="ws_security_context"></a>\_contexte de sécurité WS \_

Type opaque utilisé pour référencer un [objet de contexte de sécurité](security-context.md).


```C++
typedef struct _WS_SECURITY_CONTEXT WS_SECURITY_CONTEXT;
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

[Contexte de sécurité](security-context.md)
</dt> <dt>

[Cohérence de thread](thread-safety.md)
</dt> </dl>

 

 





