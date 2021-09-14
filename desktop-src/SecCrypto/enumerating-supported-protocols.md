---
description: Les protocoles et les suites de chiffrement pris en charge peuvent être listés par des appels à CryptGetProvParam avec PP \_ ENUMALGS ou pp \_ ENUMALGS \_ ex.
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Énumération des protocoles pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76976da7e3ab59e299d6ef0a8e9bcabce601c0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416418"
---
# <a name="enumerating-supported-protocols"></a>Énumération des protocoles pris en charge

Les protocoles et les suites de chiffrement pris en charge peuvent être listés par des appels à [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) avec pp \_ ENUMALGS ou pp \_ ENUMALGS \_ ex. La \_ valeur pp ENUMALGS \_ ex fonctionne comme pp \_ ENUMALGS, mais retourne une structure [**Prov \_ ENUMALGS \_ ex**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) qui contient des informations plus complètes sur les algorithmes pris en charge par le fournisseur.

Pour plus d’informations sur les indicateurs de protocole définis et leurs valeurs, consultez [indicateurs de protocole](protocol-flags.md).

Étant donné que le membre **hCryptProv** est le [*descripteur*](../secgloss/h-gly.md) d’un [*contexte*](../secgloss/c-gly.md) de chiffrement ouvert acquis à l’aide de [**CRYPTACQUIRECONTEXT**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) avec son paramètre *dwProvType* défini sur Prov \_ RSA \_ Schannel, l’exemple suivant répertorie les noms de tous les algorithmes disponibles dans le CSP.


```C++
PROV_ENUMALGS_EX EnumAlgs;     //   Structure to hold information on 
                               //   a supported algorithm
DWORD dFlag = CRYPT_FIRST;     //   Flag indicating that the first
                               //   supported algorithm is to be
                               //   enumerated. Changed to 0 after the
                               //   first call to the function.
cbData = sizeof(PROV_ENUMALGS_EX);

while( CryptGetProvParam(
    hCryptProv,          // handle to an open cryptographic provider
    PP_ENUMALGS_EX, 
    (BYTE *)&EnumAlgs,  // information on the next algorithm
    &cbData,            // number of bytes in the PROV_ENUMALGS_EX
    dFlag))             // flag to indicate whether this is a first or
                        // subsequent algorithm supported by the
                        // CSP.
{
    printf("Supported Algorithm name %s\n", EnumAlgs.szName);
    dFlag = CRYPT_NEXT;          // Set to CRYPT_NEXT after the first call,
} //  end of while loop. When all of the supported algorithms have
  //  been enumerated, the function returns FALSE.
```



Le tableau suivant répertorie certains algorithmes retournés par un \_ fournisseur de services de chiffrement RSA SChannel standard national Prov \_ . Notez que ni SSL2 SHA Mac ni SSL2 DES chiffrements n’est pris en charge par le fournisseur CSP dans cet exemple.



| Identificateur d’algorithme                                                                        | Longueur de clé minimale | Longueur de clé maximale | Protocoles | Nom de l'algorithme |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [*CALG \_ RSA \_ KEYX*](../secgloss/c-gly.md) | 512                | 2 048               | 0x0007    | « RSA \_ KEYX »    |
| [*CALG \_ MD5*](../secgloss/c-gly.md)                 | 128                | 128                | 0x0007    | ISSU          |
| [*CALG \_ SHA*](../secgloss/c-gly.md)                 | 160                | 160                | 0x0005    | Tcha          |
| [*CALG \_ RC4*](../secgloss/c-gly.md)                 | 40                 | 128                | 0x0007    | RC4          |
| CALG \_ des                                                                                   | 56                 | 56                 | 0x0005    | DES          |



 

Pour préparer l’envoi de messages ClientHello ou ServerHello, le moteur de protocole [*Schannel*](../secgloss/s-gly.md) énumère les algorithmes et les tailles de clé pris en charge par le CSP et crée une liste en interne des suites de chiffrement prises en charge.

 

 
