---
title: WS_SECURITY_TOKEN (WebServices. h)
description: Handle opaque représentant un jeton de sécurité.
ms.assetid: 050a2ce5-279e-48fb-85da-1d0b11cd8229
keywords:
- WS_SECURITY_TOKEN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52e69a46f206f1def7cc2e7e2d03c2e5f1369f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234365"
---
# <a name="ws_security_token"></a>\_jeton de sécurité WS \_

Handle opaque représentant un [jeton de sécurité](security-processing-results.md).


```C++
typedef struct _WS_SECURITY_TOKEN WS_SECURITY_TOKEN;
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

[Résultats du traitement de la sécurité](security-processing-results.md)
</dt> <dt>

[Cohérence de thread](thread-safety.md)
</dt> </dl>

 

 





