---
description: Le type de données TimeStamp contient des informations sur la durée de validité des jetons de sécurité. Le format de la valeur du type de données TimeStamp est le même que celui de la structure FILETIME.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: Horodateur (SSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4898e85b0c11f55e5bb0dba2dbdefe2a3b6a2e4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096305"
---
# <a name="timestamp"></a>TimeStamp

Le type de données **timestamp** contient des informations sur la durée de validité des jetons de sécurité. Le format de la valeur du type de données **timestamp** est le même que celui de la structure [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |



 

 
