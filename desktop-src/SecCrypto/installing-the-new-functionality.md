---
description: L’installation de nouvelles fonctionnalités en mémoire peut améliorer les performances. Les fonctions CryptoAPI recherchent de la mémoire pour la fonctionnalité avant de rechercher la DLL dans le registre. La DLL doit être chargée avant l’installation de la fonctionnalité.
ms.assetid: f6e5fc6a-a186-4648-af63-0555307f53d8
title: Installation des nouvelles fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7147a1a70ffe57f4948d7db94aab0184d29e5dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534739"
---
# <a name="installing-the-new-functionality"></a><span data-ttu-id="21863-105">Installation des nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="21863-105">Installing the New Functionality</span></span>

<span data-ttu-id="21863-106">L’installation de nouvelles fonctionnalités en mémoire peut améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="21863-106">Installing new functionality into memory can improve performance.</span></span> <span data-ttu-id="21863-107">Les fonctions [*CryptoAPI*](../secgloss/c-gly.md) recherchent de la mémoire pour la fonctionnalité avant de rechercher la dll dans le registre.</span><span class="sxs-lookup"><span data-stu-id="21863-107">[*CryptoAPI*](../secgloss/c-gly.md) functions search memory for the functionality before searching the registry for the DLL.</span></span> <span data-ttu-id="21863-108">La DLL doit être chargée avant l’installation de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="21863-108">The DLL must be loaded before installing the functionality.</span></span>

<span data-ttu-id="21863-109">[**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) installe l’adresse de la nouvelle fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="21863-109">[**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) installs the address of the new functionality.</span></span> <span data-ttu-id="21863-110">Elle doit être placée dans la fonction **DllMain** de la dll.</span><span class="sxs-lookup"><span data-stu-id="21863-110">It should be placed in the **DllMain** function of the DLL.</span></span>

<span data-ttu-id="21863-111">Si *HMODULE* est passé à [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress), une fois installé, la dll n’est pas déchargée tant que le Crypt32.dll n’est pas déchargé.</span><span class="sxs-lookup"><span data-stu-id="21863-111">If *hModule* is passed to [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress), once installed, the DLL is not unloaded until the Crypt32.dll is unloaded.</span></span>

<span data-ttu-id="21863-112">L’exemple suivant appelle la fonction [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) .</span><span class="sxs-lookup"><span data-stu-id="21863-112">The following example calls the [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) function.</span></span>


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



 

 
