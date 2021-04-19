---
description: Une fois la clé principale créée ou importée, RSA/SChannel et Diffie-Hellman/Schannel informent le CSP du type des clés de chiffrement en bloc et des clés MAC qui seront dérivées de la clé principale.
ms.assetid: d0976a7e-3c8e-4bbe-80e1-568a27ab81c6
title: Spécification des algorithmes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5d329486c655fbc347d35870cfe81335678cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515677"
---
# <a name="specifying-the-algorithms"></a><span data-ttu-id="f7601-103">Spécification des algorithmes</span><span class="sxs-lookup"><span data-stu-id="f7601-103">Specifying the Algorithms</span></span>

<span data-ttu-id="f7601-104">Une fois qu’une [*clé principale*](../secgloss/m-gly.md) est créée ou importée, [*RSA*](../secgloss/r-gly.md)/Schannel et [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel informent le [*CSP*](../secgloss/c-gly.md) du type des [*clés de chiffrement en bloc*](../secgloss/b-gly.md) et des [*clés Mac*](../secgloss/m-gly.md) qui seront dérivées de la clé principale.</span><span class="sxs-lookup"><span data-stu-id="f7601-104">After a [*master key*](../secgloss/m-gly.md) is created or imported, both [*RSA*](../secgloss/r-gly.md)/Schannel and [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel inform the [*CSP*](../secgloss/c-gly.md) of the type of [*bulk encryption keys*](../secgloss/b-gly.md) and [*MAC keys*](../secgloss/m-gly.md) that will be derived from the master key.</span></span> <span data-ttu-id="f7601-105">L’exemple suivant spécifie ces algorithmes.</span><span class="sxs-lookup"><span data-stu-id="f7601-105">The following example specifies these algorithms.</span></span> <span data-ttu-id="f7601-106">Le même code est utilisé pour le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="f7601-106">The same code is used for both client and server.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

typedef struct _SCHANNEL_ALG 
{
    DWORD  dwUse;
    ALG_ID Algid;
    DWORD  cBits;
    DWORD  dwFlags;
    DWORD  dwReserved;
} SCHANNEL_ALG, *PSCHANNEL_ALG;

SCHANNEL_ALG Algorithm;

//--------------------------------------------------------------------
// Algorithms for the SCHANNEL_ALG structure

#define SCHANNEL_MAC_KEY   0x00000000
#define SCHANNEL_ENC_KEY   0x00000001

//--------------------------------------------------------------------
// dwFlags for the SCHANNEL_ALG structure
// This flag will be set when the SSL cipher suite is exportable 
// outside the United States and Canada. The use of this flag notifies
// the CSP that it must perform the extra export steps when deriving 
// the key.

#define INTERNATIONAL USAGE   0x00000001

void main()
{
//--------------------------------------------------------------------
// Specify the bulk encryption algorithm.

Algorithm.dwUse = SCHANNEL_ENC_KEY;
Algorithm.Algid = CALG_RC4;    // or CALG_RC2, CALG_DES, and so on
Algorithm.cBits = 40;          // or 64, 128, 192, and so on
if (!CryptSetKeyParam(
         hMasterKey, 
         KP_SCHANNEL_ALG, 
         (PBYTE)&Algorithm, 
         0))
{
    printf("Failed called to CryptSetKeyParam\n");
    exit(1);
};

//--------------------------------------------------------------------
// Specify hash algorithm.
Algorithm.dwUse = SCHANNEL_MAC_KEY;
Algorithm.Algid = CALG_MD5;    // or CALG_SHA, and so on
Algorithm.cBits = 128;         // or 160...
if (!CryptSetKeyParam(
          hMasterKey, 
          KP_SCHANNEL_ALG, 
          (PBYTE)&Algorithm, 
          0))
{
    printf("Failed called to CryptSetKeyParam\n");
    exit(1);
};
```



> [!Note]  
> <span data-ttu-id="f7601-107">Un moteur de protocole [*Schannel*](../secgloss/s-gly.md) ne doit pas spécifier les algorithmes et les tailles de clé non pris en charge par le fournisseur CSP.</span><span class="sxs-lookup"><span data-stu-id="f7601-107">An [*Schannel*](../secgloss/s-gly.md) protocol engine must not specify algorithms and key sizes not supported by the CSP.</span></span> <span data-ttu-id="f7601-108">Pour plus d’informations, consultez [énumération des protocoles pris en charge](enumerating-supported-protocols.md).</span><span class="sxs-lookup"><span data-stu-id="f7601-108">For more information, see [Enumerating Supported Protocols](enumerating-supported-protocols.md).</span></span> <span data-ttu-id="f7601-109">Si des algorithmes ou des tailles de clé non pris en charge sont spécifiés, la fonction CSP doit échouer et retourner le \_ code d’erreur de données erronées NPD \_ .</span><span class="sxs-lookup"><span data-stu-id="f7601-109">If unsupported algorithms or key sizes are specified, the CSP function must fail and return the NTE\_BAD\_DATA error code.</span></span>

 

 

 
