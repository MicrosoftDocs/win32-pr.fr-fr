---
description: Représente un handle vers une fonction d’installation d’identificateur d’objet (OID).
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: HCRYPTOIDFUNCADDR (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fb36bdd98332842d89533c9c34a880aecdc8555cd64bb03888c0bd146cea3f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006547"
---
# <a name="hcryptoidfuncaddr"></a>HCRYPTOIDFUNCADDR

Le type de données **HCRYPTOIDFUNCADDR** représente un handle vers une fonction d’installation d' [*identificateur d’objet*](../secgloss/o-gly.md) (OID). Les fonctions [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)et [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) , ainsi que la structure d' [**\_ \_ \_ informations Prov Store store**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) , utilisent ce type de données.


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
