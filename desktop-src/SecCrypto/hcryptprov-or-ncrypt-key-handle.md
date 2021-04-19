---
description: Est utilisé comme handle d’un fournisseur de services de chiffrement CryptoAPI (CSP) ou CSP CNG.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbd442b93cdb9ba7479878aa9fcad095b7903af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532142"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a>\_handle de clé HCRYPTPROV ou \_ NCRYPT \_ \_

Le type de données du **\_ handle de clé HCRYPTPROV ou \_ NCRYPT \_ \_** est utilisé comme handle d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) CryptoAPI ou d’un CSP CNG. Ce handle doit être un handle [**HCRYPTPROV**](hcryptprov.md) qui a été créé à l’aide de la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) ou d’un handle de **\_ \_ handle de clé NCRYPT** créé à l’aide de la fonction [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) . Les nouvelles applications doivent toujours passer le descripteur de **\_ \_ handle de clé NCRYPT** à un CSP CNG.


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
