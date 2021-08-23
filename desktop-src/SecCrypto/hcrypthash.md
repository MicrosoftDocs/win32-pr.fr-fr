---
description: Le type de données HCRYPTHASH est utilisé pour représenter les descripteurs des objets de hachage.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: HCRYPTHASH (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b2d20d7aeb46adda162f8d5ec380143164690bad8ee88139f9653753f1e290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006557"
---
# <a name="hcrypthash"></a>HCRYPTHASH

Le type de données **HCRYPTHASH** est utilisé pour représenter les descripteurs des [*objets de hachage*](../secgloss/h-gly.md). Ces handles indiquent au module CSP le hachage utilisé dans une opération particulière. Le module CSP n’active pas la manipulation directe des valeurs de hachage. Au lieu de cela, l’utilisateur manipule les valeurs de hachage par le biais du handle de hachage.


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
