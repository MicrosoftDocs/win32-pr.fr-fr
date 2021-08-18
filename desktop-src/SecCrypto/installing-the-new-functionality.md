---
description: L’installation de nouvelles fonctionnalités en mémoire peut améliorer les performances. Les fonctions CryptoAPI recherchent de la mémoire pour la fonctionnalité avant de rechercher la DLL dans le registre. La DLL doit être chargée avant l’installation de la fonctionnalité.
ms.assetid: f6e5fc6a-a186-4648-af63-0555307f53d8
title: Installation des nouvelles fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c71167f8226ad78f449b3f529e2e22bdb060bc0c5d984671cf4c5a30cc6f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005297"
---
# <a name="installing-the-new-functionality"></a>Installation des nouvelles fonctionnalités

L’installation de nouvelles fonctionnalités en mémoire peut améliorer les performances. Les fonctions [*CryptoAPI*](../secgloss/c-gly.md) recherchent de la mémoire pour la fonctionnalité avant de rechercher la dll dans le registre. La DLL doit être chargée avant l’installation de la fonctionnalité.

[**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) installe l’adresse de la nouvelle fonctionnalité. Elle doit être placée dans la fonction **DllMain** de la dll.

Si *HMODULE* est passé à [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress), une fois installé, la dll n’est pas déchargée tant que le Crypt32.dll n’est pas déchargé.

L’exemple suivant appelle la fonction [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) .


```C++
#include <windows.h>
#include <stdio.h>

#define X509_ENCODE_FUNC_COUNT (sizeof(X509EncodeFuncTable) / \
                                sizeof(X509EncodeFuncTable[0]))

static BOOL WINAPI OssX509CtlUsageEncode(
        IN DWORD dwCertEncodingType,
        IN LPCSTR lpszStructType,
        IN PCTL_USAGE pInfo,
        OUT BYTE *pbEncoded,
        IN OUT DWORD *pcbEncoded
);

static const CRYPT_OID_FUNC_ENTRY X509EncodeFuncTable[] = {
    X509_ENHANCED_KEY_USAGE, OssX509CtlUsageEncode,
};

BOOL WINAPI DllMain(
    HMODULE hModule,
    ULONG  ulReason,
    LPVOID lpReserved)
{
    switch (ulReason)
    {
        case DLL_PROCESS_ATTACH:
            if (!CryptInstallOIDFunctionAddress(
                  hModule,
                  X509_ASN_ENCODING,
                  CRYPT_OID_ENCODE_OBJECT_FUNC,
                  X509_ENCODE_FUNC_COUNT,
                  X509EncodeFuncTable,
                  0))
            {
                printf("Install OID function address failed."); 
                return FALSE;
            }
            break;
         default:
            break;
    }
    return TRUE;
}

//-------------------------------------------------------------------
//  CTL Usage (Enhanced Key Usage) Encode (OSS X509)
//-------------------------------------------------------------------
static BOOL WINAPI OssX509CtlUsageEncode(
        IN DWORD /*dwCertEncodingType*/,
        IN LPCSTR /*lpszStructType*/,
        IN PCTL_USAGE pInfo,
        OUT BYTE *pbEncoded,
        IN OUT DWORD *pcbEncoded)
{
    //Encoding logic goes here.
}
```



 

 
