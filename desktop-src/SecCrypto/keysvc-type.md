---
description: L' \_ énumération de type KEYSVC définit si une clé s’applique à un ordinateur ou à un service.
ms.assetid: 573a412a-1e9d-47ac-bd09-2319d4b9712b
title: Énumération KEYSVC_TYPE (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_TYPE
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 3c23cc259029cf76fcb1590e6261623827d59b48c9a0728e21c8250ca3e858f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976092"
---
# <a name="keysvc_type-enumeration"></a>\_Énumération de type KEYSVC

L’énumération de **\_ type KEYSVC** définit si une clé s’applique à un ordinateur ou à un service.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _KEYSVC_TYPE { 
  KeySvcMachine,
  KeySvcService
} KEYSVC_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="KeySvcMachine"></span><span id="keysvcmachine"></span><span id="KEYSVCMACHINE"></span>**KeySvcMachine**
</dt> <dd>

La clé est destinée à un ordinateur.

</dd> <dt>

<span id="KeySvcService"></span><span id="keysvcservice"></span><span id="KEYSVCSERVICE"></span>**KeySvcService**
</dt> <dd>

La clé concerne un service.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 




