---
description: Type de données opaque.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (Ntsecpkg. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 792b81516e434469750b4ddd667bf6ddb82df31f4f13f82588d281f743bc8835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921038"
---
# <a name="plsa_client_request"></a>\_demande du client PLSA \_

Le type de données de la **\_ \_ demande du client PLSA** est un type de données opaque.

L' [*autorité de sécurité locale (LSA, Local Security Authority*](../secgloss/l-gly.md) ) l’utilise en interne pour gérer les informations du client relatives aux demandes individuelles.


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Ntsecpkg. h</dt> </dl> |



 

 
