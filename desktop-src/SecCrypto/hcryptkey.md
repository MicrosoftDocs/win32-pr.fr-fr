---
description: Le type de données HCRYPTKEY est utilisé pour représenter les descripteurs des clés de chiffrement.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: HCRYPTKEY (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56bda14169aa2f4d7c6e502d3444473ea0f00408
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233333"
---
# <a name="hcryptkey"></a>HCRYPTKEY

Le type de données **HCRYPTKEY** est utilisé pour représenter les descripteurs des [*clés de chiffrement*](../secgloss/c-gly.md). Ces descripteurs sont utilisés pour indiquer au module CSP quelle clé est utilisée dans une opération spécifique. Le module CSP n’autorise pas l’accès direct aux valeurs de clé. Au lieu de cela, l’utilisateur exécute des fonctions à l’aide de la valeur de clé par le biais du handle de clé.


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
