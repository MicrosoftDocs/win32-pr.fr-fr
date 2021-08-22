---
description: Le type de données HCRYPTKEY est utilisé pour représenter les descripteurs des clés de chiffrement.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: HCRYPTKEY (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78d50f7fb005d877f6520172631b4546b8d498c415de58502defd26831c65fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006437"
---
# <a name="hcryptkey"></a>HCRYPTKEY

Le type de données **HCRYPTKEY** est utilisé pour représenter les descripteurs des [*clés de chiffrement*](../secgloss/c-gly.md). Ces descripteurs sont utilisés pour indiquer au module CSP quelle clé est utilisée dans une opération spécifique. Le module CSP n’autorise pas l’accès direct aux valeurs de clé. Au lieu de cela, l’utilisateur exécute des fonctions à l’aide de la valeur de clé par le biais du handle de clé.


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
