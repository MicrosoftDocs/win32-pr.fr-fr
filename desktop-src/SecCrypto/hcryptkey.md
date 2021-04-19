---
description: Le type de données HCRYPTKEY est utilisé pour représenter les descripteurs des clés de chiffrement.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: HCRYPTKEY (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56bda14169aa2f4d7c6e502d3444473ea0f00408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530158"
---
# <a name="hcryptkey"></a>HCRYPTKEY

Le type de données **HCRYPTKEY** est utilisé pour représenter les descripteurs des [*clés de chiffrement*](../secgloss/c-gly.md). Ces descripteurs sont utilisés pour indiquer au module CSP quelle clé est utilisée dans une opération spécifique. Le module CSP n’autorise pas l’accès direct aux valeurs de clé. Au lieu de cela, l’utilisateur exécute des fonctions à l’aide de la valeur de clé par le biais du handle de clé.


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
