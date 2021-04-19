---
description: Les protocoles et les suites de chiffrement pris en charge peuvent être listés par des appels à CryptGetProvParam avec PP \_ ENUMALGS ou pp \_ ENUMALGS \_ ex.
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Énumération des protocoles pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76976da7e3ab59e299d6ef0a8e9bcabce601c0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534209"
---
# <a name="enumerating-supported-protocols"></a><span data-ttu-id="d3ca4-103">Énumération des protocoles pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3ca4-103">Enumerating Supported Protocols</span></span>

<span data-ttu-id="d3ca4-104">Les protocoles et les suites de chiffrement pris en charge peuvent être listés par des appels à [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) avec pp \_ ENUMALGS ou pp \_ ENUMALGS \_ ex.</span><span class="sxs-lookup"><span data-stu-id="d3ca4-104">Supported protocols and cipher suites can be listed by calls to [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with PP\_ENUMALGS or PP\_ENUMALGS\_EX.</span></span> <span data-ttu-id="d3ca4-105">La \_ valeur pp ENUMALGS \_ ex fonctionne comme pp \_ ENUMALGS, mais retourne une structure [**Prov \_ ENUMALGS \_ ex**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) qui contient des informations plus complètes sur les algorithmes pris en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d3ca4-105">The PP\_ENUMALGS\_EX value works like PP\_ENUMALGS but returns a [**PROV\_ENUMALGS\_EX**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) structure that holds more extensive information on the algorithms supported by the provider.</span></span>

<span data-ttu-id="d3ca4-106">Pour plus d’informations sur les indicateurs de protocole définis et leurs valeurs, consultez [indicateurs de protocole](protocol-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d3ca4-106">For more information about defined protocol flags and their values, see [Protocol Flags](protocol-flags.md).</span></span>

<span data-ttu-id="d3ca4-107">Étant donné que le membre **hCryptProv** est le [*descripteur*](../secgloss/h-gly.md) d’un [*contexte*](../secgloss/c-gly.md) de chiffrement ouvert acquis à l’aide de [**CRYPTACQUIRECONTEXT**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) avec son paramètre *dwProvType* défini sur Prov \_ RSA \_ Schannel, l’exemple suivant répertorie les noms de tous les algorithmes disponibles dans le CSP.</span><span class="sxs-lookup"><span data-stu-id="d3ca4-107">Given that the **hCryptProv** member is the [*handle*](../secgloss/h-gly.md) of an open cryptographic [*context*](../secgloss/c-gly.md) acquired by using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) with its *dwProvType* parameter set to PROV\_RSA\_SCHANNEL, the following example lists the names of all algorithms available in the CSP.</span></span>


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



<span data-ttu-id="d3ca4-108">Le tableau suivant répertorie certains algorithmes retournés par un \_ fournisseur de services de chiffrement RSA SChannel standard national Prov \_ .</span><span class="sxs-lookup"><span data-stu-id="d3ca4-108">The following table lists some algorithms returned by a typical domestic PROV\_RSA\_SCHANNEL CSP.</span></span> <span data-ttu-id="d3ca4-109">Notez que ni SSL2 SHA Mac ni SSL2 DES chiffrements n’est pris en charge par le fournisseur CSP dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="d3ca4-109">Notice that neither SSL2 SHA MACs nor SSL2 DES encryption is supported by the CSP in this example.</span></span>



| <span data-ttu-id="d3ca4-110">Identificateur d’algorithme</span><span class="sxs-lookup"><span data-stu-id="d3ca4-110">Algorithm identifier</span></span>                                                                        | <span data-ttu-id="d3ca4-111">Longueur de clé minimale</span><span class="sxs-lookup"><span data-stu-id="d3ca4-111">Minimum key length</span></span> | <span data-ttu-id="d3ca4-112">Longueur de clé maximale</span><span class="sxs-lookup"><span data-stu-id="d3ca4-112">Maximum key length</span></span> | <span data-ttu-id="d3ca4-113">Protocoles</span><span class="sxs-lookup"><span data-stu-id="d3ca4-113">Protocols</span></span> | <span data-ttu-id="d3ca4-114">Nom de l'algorithme</span><span class="sxs-lookup"><span data-stu-id="d3ca4-114">Algorithm name</span></span> |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [<span data-ttu-id="d3ca4-115">*CALG \_ RSA \_ KEYX*</span><span class="sxs-lookup"><span data-stu-id="d3ca4-115">*CALG\_RSA\_KEYX*</span></span>](../secgloss/c-gly.md) | <span data-ttu-id="d3ca4-116">512</span><span class="sxs-lookup"><span data-stu-id="d3ca4-116">512</span></span>                | <span data-ttu-id="d3ca4-117">2 048</span><span class="sxs-lookup"><span data-stu-id="d3ca4-117">2048</span></span>               | <span data-ttu-id="d3ca4-118">0x0007</span><span class="sxs-lookup"><span data-stu-id="d3ca4-118">0x0007</span></span>    | <span data-ttu-id="d3ca4-119">« RSA \_ KEYX »</span><span class="sxs-lookup"><span data-stu-id="d3ca4-119">"RSA\_KEYX"</span></span>    |
| [<span data-ttu-id="d3ca4-120">*CALG \_ MD5*</span><span class="sxs-lookup"><span data-stu-id="d3ca4-120">*CALG\_MD5*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="d3ca4-121">128</span><span class="sxs-lookup"><span data-stu-id="d3ca4-121">128</span></span>                | <span data-ttu-id="d3ca4-122">128</span><span class="sxs-lookup"><span data-stu-id="d3ca4-122">128</span></span>                | <span data-ttu-id="d3ca4-123">0x0007</span><span class="sxs-lookup"><span data-stu-id="d3ca4-123">0x0007</span></span>    | <span data-ttu-id="d3ca4-124">ISSU</span><span class="sxs-lookup"><span data-stu-id="d3ca4-124">"MD5"</span></span>          |
| [<span data-ttu-id="d3ca4-125">*CALG \_ SHA*</span><span class="sxs-lookup"><span data-stu-id="d3ca4-125">*CALG\_SHA*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="d3ca4-126">160</span><span class="sxs-lookup"><span data-stu-id="d3ca4-126">160</span></span>                | <span data-ttu-id="d3ca4-127">160</span><span class="sxs-lookup"><span data-stu-id="d3ca4-127">160</span></span>                | <span data-ttu-id="d3ca4-128">0x0005</span><span class="sxs-lookup"><span data-stu-id="d3ca4-128">0x0005</span></span>    | <span data-ttu-id="d3ca4-129">Tcha</span><span class="sxs-lookup"><span data-stu-id="d3ca4-129">"SHA"</span></span>          |
| [<span data-ttu-id="d3ca4-130">*CALG \_ RC4*</span><span class="sxs-lookup"><span data-stu-id="d3ca4-130">*CALG\_RC4*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="d3ca4-131">40</span><span class="sxs-lookup"><span data-stu-id="d3ca4-131">40</span></span>                 | <span data-ttu-id="d3ca4-132">128</span><span class="sxs-lookup"><span data-stu-id="d3ca4-132">128</span></span>                | <span data-ttu-id="d3ca4-133">0x0007</span><span class="sxs-lookup"><span data-stu-id="d3ca4-133">0x0007</span></span>    | <span data-ttu-id="d3ca4-134">RC4</span><span class="sxs-lookup"><span data-stu-id="d3ca4-134">"RC4"</span></span>          |
| <span data-ttu-id="d3ca4-135">CALG \_ des</span><span class="sxs-lookup"><span data-stu-id="d3ca4-135">CALG\_DES</span></span>                                                                                   | <span data-ttu-id="d3ca4-136">56</span><span class="sxs-lookup"><span data-stu-id="d3ca4-136">56</span></span>                 | <span data-ttu-id="d3ca4-137">56</span><span class="sxs-lookup"><span data-stu-id="d3ca4-137">56</span></span>                 | <span data-ttu-id="d3ca4-138">0x0005</span><span class="sxs-lookup"><span data-stu-id="d3ca4-138">0x0005</span></span>    | <span data-ttu-id="d3ca4-139">DES</span><span class="sxs-lookup"><span data-stu-id="d3ca4-139">"DES"</span></span>          |



 

<span data-ttu-id="d3ca4-140">Pour préparer l’envoi de messages ClientHello ou ServerHello, le moteur de protocole [*Schannel*](../secgloss/s-gly.md) énumère les algorithmes et les tailles de clé pris en charge par le CSP et crée une liste en interne des suites de chiffrement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d3ca4-140">To prepare to send ClientHello or ServerHello messages, the [*Schannel*](../secgloss/s-gly.md) protocol engine enumerates the algorithms and key sizes supported by the CSP and builds a list internally of supported cipher suites.</span></span>

 

 
