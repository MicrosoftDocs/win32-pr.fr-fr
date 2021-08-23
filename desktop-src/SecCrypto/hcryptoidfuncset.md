---
description: Représente un handle vers un ensemble de fonctions installables d’identificateur d’objet (OID).
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: HCRYPTOIDFUNCSET (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3926b78359450b780a9952aeae9d957157ebb56973a7f428824b07cbb43e9a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006467"
---
# <a name="hcryptoidfuncset"></a>HCRYPTOIDFUNCSET

Le type de données **HCRYPTOIDFUNCSET** représente un descripteur d’un ensemble de fonctions d' [*identificateur d’objet*](../secgloss/o-gly.md) (OID) installables. Les fonctions [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)et [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) utilisent ce type de données.


```C++
typedef void* HCRYPTOIDFUNCSET;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
