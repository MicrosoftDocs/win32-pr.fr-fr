---
description: Le fournisseur de base a utilisé uniquement des clés symétriques 40 bits.
ms.assetid: 7cfa6c7e-e30c-4829-9989-9567b42ad92f
title: Nouvelles fonctionnalités de longueur de clé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6842bfc1f4e68f115d804a55d628ffa51f0c68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210240"
---
# <a name="new-key-length-functionality"></a><span data-ttu-id="92606-103">Nouvelles fonctionnalités de longueur de clé</span><span class="sxs-lookup"><span data-stu-id="92606-103">New Key-length Functionality</span></span>

<span data-ttu-id="92606-104">Le fournisseur de base a utilisé uniquement des [*clés symétriques*](../secgloss/s-gly.md)40 bits.</span><span class="sxs-lookup"><span data-stu-id="92606-104">The Base Provider used only 40-bit [*symmetric keys*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="92606-105">L’ajout de clés plus longues dans le fournisseur amélioré et le fait que les clés importées peuvent être de longueur arbitraire nécessitent une méthode d’interrogation de la longueur d’une clé spécifique.</span><span class="sxs-lookup"><span data-stu-id="92606-105">The addition of longer keys in the Enhanced Provider, and the fact that imported keys can be of arbitrary length requires a method of querying the length for a specific key.</span></span> <span data-ttu-id="92606-106">Pour rechercher la longueur réelle d’une clé en bits, un utilisateur peut appeler [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) avec la \_ valeur de paramètre KP KEYLEN.</span><span class="sxs-lookup"><span data-stu-id="92606-106">To find the actual length of a key in bits, a user can call [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) with the KP\_KEYLEN parameter value.</span></span> <span data-ttu-id="92606-107">La longueur de la clé est retournée dans la **valeur DWORD** désignée par le paramètre *pbData* .</span><span class="sxs-lookup"><span data-stu-id="92606-107">The length of the key is returned in the **DWORD** pointed to by the *pbData* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="92606-108">Pour vous protéger contre les attaques [*Cryptanalysis*](../secgloss/c-gly.md) pas à pas, les applications doivent vérifier les [*longueurs de clé*](../secgloss/k-gly.md) insuffisantes et notifier l’utilisateur lorsqu’il rencontre une erreur.</span><span class="sxs-lookup"><span data-stu-id="92606-108">To protect against stepping-down [*cryptanalysis*](../secgloss/c-gly.md) attacks, applications must check for insufficient [*key lengths*](../secgloss/k-gly.md) and notify the user when one is encountered.</span></span>

 

<span data-ttu-id="92606-109">L’exemple suivant montre comment interroger la longueur d’une clé.</span><span class="sxs-lookup"><span data-stu-id="92606-109">The following example shows how to query the length of a key.</span></span>


```C++
#pragma comment(lib, "crypt32.lib")

#include <windows.h>
#include <Wincrypt.h>
#include <stdio.h>
void main()
{
    HCRYPTPROV hProv = NULL;
    HCRYPTKEY hKey = NULL;

    DWORD dwKeyLength;
    DWORD dwLen = sizeof(DWORD);
    // Copyright (C) Microsoft.  All rights reserved.
    // Acquire a cryptographic context.
    if (!CryptAcquireContext(&hProv,
                              NULL,
                              NULL,
                              PROV_RSA_FULL,
                              CRYPT_VERIFYCONTEXT))
    {
        printf("CryptAcquireContext failed.\n");
        goto Cleanup;
    }

    // Generate a key.
    if (!CryptGenKey(
                hProv,    
                CALG_RC2,    
                0,    
                &hKey))
    {
        printf("CryptGenKey failed.\n");
        goto Cleanup;
    }

    // Query the key length.
    if (!CryptGetKeyParam(
            hKey,    
            KP_KEYLEN,    
            (BYTE*)&dwKeyLength,
            &dwLen,    
            0))
    {
        printf("CryptGetKeyParam failed.\n");
        goto Cleanup;
    }
    else
    {
        printf("The key is %d bits long. \n", dwKeyLength);
    } 

Cleanup:

    if (hKey)
        CryptDestroyKey(hKey);

    if (hProv)
        CryptReleaseContext(hProv, 0);
}
```



 

 
