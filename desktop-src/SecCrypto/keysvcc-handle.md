---
description: Le \_ type de données handle KEYSVCC définit un handle de service de clé. Un \_ handle de handle KEYSVCC est utilisé par les fonctions RKeyOpenKeyService et RKeyCloseKeyService.
ms.assetid: d0fd5184-5c8e-4f96-9ff1-8abd6f718d05
title: KEYSVCC_HANDLE (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32e34285c6291cb7cb87aeb9095e5261b43999b0eefa82e33704719e7673f1b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515949"
---
# <a name="keysvcc_handle"></a>\_handle KEYSVCC

Le type de données **\_ handle KEYSVCC** définit un handle de service de clé. Un handle de **\_ handle KEYSVCC** est utilisé par les fonctions [**RKeyOpenKeyService**](rkeyopenkeyservice.md) et [**RKeyCloseKeyService**](rkeyclosekeyservice.md) .


```C++
typedef void* KEYSVCC_HANDLE;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 




