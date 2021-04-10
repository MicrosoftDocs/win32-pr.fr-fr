---
description: Le type de données HCRYPTHASH est utilisé pour représenter les descripteurs des objets de hachage.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: HCRYPTHASH (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a009350ed910627c1e6ec9ae33997ed20c7fec2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867413"
---
# <a name="hcrypthash"></a>HCRYPTHASH

Le type de données **HCRYPTHASH** est utilisé pour représenter les descripteurs des [*objets de hachage*](../secgloss/h-gly.md). Ces handles indiquent au module CSP le hachage utilisé dans une opération particulière. Le module CSP n’active pas la manipulation directe des valeurs de hachage. Au lieu de cela, l’utilisateur manipule les valeurs de hachage par le biais du handle de hachage.


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
