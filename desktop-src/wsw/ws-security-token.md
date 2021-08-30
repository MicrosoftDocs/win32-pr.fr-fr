---
title: WS_SECURITY_TOKEN (WebServices. h)
description: Handle opaque représentant un jeton de sécurité.
ms.assetid: 050a2ce5-279e-48fb-85da-1d0b11cd8229
keywords:
- WS_SECURITY_TOKEN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9b577188e5dbd718de36703aec4602f9dcc94f28a74fa45f8f66af49ccdd5cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109659"
---
# <a name="ws_security_token"></a>\_jeton de sécurité WS \_

Handle opaque représentant un [jeton de sécurité](security-processing-results.md).


```C++
typedef struct _WS_SECURITY_TOKEN WS_SECURITY_TOKEN;
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

[Résultats du traitement de la sécurité](security-processing-results.md)
</dt> <dt>

[Cohérence de thread](thread-safety.md)
</dt> </dl>

 

 





