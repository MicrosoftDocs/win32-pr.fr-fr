---
title: RPC_STATUS (rpcdce. h)
description: L’état RPC du type de données \_ représente un type de code d’état spécifique à la plateforme.
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93cc6f682dbb46b65fc261b738b94e8000f3a77d96c4bd65d1fead4bf8c0e17a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925986"
---
# <a name="rpc_status"></a>\_état RPC

L' **\_ état RPC** du type de données représente un type de code d’état spécifique à la plateforme.


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a>Remarques

Le type d' **\_ état RPC** est retourné par la plupart des fonctions RPC et fait partie de la définition du type de fonction [**\_ \_ INQ \_ FN de l’objet RPC**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>Rpcdce. h (inclure RPC. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_objet RPC \_ INQ \_ FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





