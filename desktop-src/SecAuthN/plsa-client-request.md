---
description: Type de données opaque.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (Ntsecpkg. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3685c3cd38843edfd4ae708a18761b6ee698c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203045"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Ntsecpkg. h</dt> </dl> |



 

 
