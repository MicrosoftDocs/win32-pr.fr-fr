---
description: Les objets BLOB sont utilisés avec le fournisseur Diffie-Hellman pour exporter des clés et importer des clés dans, le fournisseur de services de chiffrement (CSP).
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: Objets BLOB de clé de Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9194a9c12542fc0acf36aa0064a2f3e304e25f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543500"
---
# <a name="diffie-hellman-key-blobs"></a><span data-ttu-id="4680f-103">Objets BLOB de clé de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="4680f-103">Diffie-Hellman Key BLOBs</span></span>

<span data-ttu-id="4680f-104">Les [*objets BLOB*](../secgloss/b-gly.md) sont utilisés avec le fournisseur [*Diffie-Hellman*](../secgloss/d-gly.md) pour exporter des clés et importer des clés dans, le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="4680f-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Diffie-Hellman*](../secgloss/d-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="4680f-105">Objets BLOB de clé publique</span><span class="sxs-lookup"><span data-stu-id="4680f-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="4680f-106">Objets BLOB de clé privée</span><span class="sxs-lookup"><span data-stu-id="4680f-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="4680f-107">Objets BLOB de clé publique</span><span class="sxs-lookup"><span data-stu-id="4680f-107">Public Key BLOBs</span></span>

<span data-ttu-id="4680f-108">Diffie-Hellman [*objets BLOB de clé publique*](../secgloss/p-gly.md), de type **publicKeyBlob**, sont utilisés pour échanger la valeur (G ^ X) mod P dans un échange de clés Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="4680f-108">Diffie-Hellman [*public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to exchange the (G^X) mod P value in a Diffie-Hellman key exchange.</span></span> <span data-ttu-id="4680f-109">Ces clés sont exportées et importées sous la forme d’une séquence d’octets au format suivant.</span><span class="sxs-lookup"><span data-stu-id="4680f-109">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

<span data-ttu-id="4680f-110">Le tableau suivant décrit chaque composant de l' [*objet blob de clé*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4680f-110">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="4680f-111">Champ</span><span class="sxs-lookup"><span data-stu-id="4680f-111">Field</span></span>          | <span data-ttu-id="4680f-112">Description</span><span class="sxs-lookup"><span data-stu-id="4680f-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4680f-113">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="4680f-113">dhpubkey</span></span>       | <span data-ttu-id="4680f-114">Structure [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="4680f-114">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="4680f-115">Le membre **magique** doit être défini sur 0x31484400.</span><span class="sxs-lookup"><span data-stu-id="4680f-115">The **magic** member should be set to 0x31484400.</span></span> <span data-ttu-id="4680f-116">Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de « DH1 ».</span><span class="sxs-lookup"><span data-stu-id="4680f-116">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of "DH1".</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="4680f-117">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="4680f-117">publickeystruc</span></span> | <span data-ttu-id="4680f-118">Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="4680f-118">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="4680f-119">y</span><span class="sxs-lookup"><span data-stu-id="4680f-119">y</span></span>              | <span data-ttu-id="4680f-120">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="4680f-120">A **BYTE** sequence.</span></span> <span data-ttu-id="4680f-121">La valeur Y, (G ^ X) mod P, est située directement après la structure [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) et doit toujours être la longueur, en octets, du champ **DHPUBKEY bitlen** (longueur binaire de P) divisé par huit.</span><span class="sxs-lookup"><span data-stu-id="4680f-121">The Y value, (G^X) mod P, is located directly after the [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure, and should always be the length, in bytes, of the **DHPUBKEY bitlen** field (bit length of P) divided by eight.</span></span> <span data-ttu-id="4680f-122">Si la longueur des données résultant du calcul de (G ^ X) mod P est un ou plusieurs octets plus courts que P divisés par huit, les données doivent être complétées par les octets nécessaires (de zéro valeur) pour que les données soient de la longueur souhaitée (format [*Little endian*](../secgloss/l-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="4680f-122">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by eight, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |



 

## <a name="private-key-blobs"></a><span data-ttu-id="4680f-123">Objets BLOB de clé privée</span><span class="sxs-lookup"><span data-stu-id="4680f-123">Private Key BLOBs</span></span>

<span data-ttu-id="4680f-124">Diffie-Hellman [*objets BLOB de clé privée*](../secgloss/p-gly.md), tapez **PRIVATEKEYBLOB**, sont utilisés pour stocker les informations publiques/privées d’une clé de Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="4680f-124">Diffie-Hellman [*private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store the public/private information of a Diffie-Hellman key.</span></span> <span data-ttu-id="4680f-125">Ces clés sont exportées et importées sous la forme d’une séquence d’octets au format suivant.</span><span class="sxs-lookup"><span data-stu-id="4680f-125">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

<span data-ttu-id="4680f-126">Le tableau suivant décrit chaque composant de l’objet BLOB de clé.</span><span class="sxs-lookup"><span data-stu-id="4680f-126">The following table describes each component of the key BLOB.</span></span>



| <span data-ttu-id="4680f-127">Champ</span><span class="sxs-lookup"><span data-stu-id="4680f-127">Field</span></span>          | <span data-ttu-id="4680f-128">Description</span><span class="sxs-lookup"><span data-stu-id="4680f-128">Description</span></span>                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4680f-129">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="4680f-129">dhpubkey</span></span>       | <span data-ttu-id="4680f-130">Structure [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="4680f-130">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="4680f-131">Le membre **magique** doit être défini sur 0x32484400.</span><span class="sxs-lookup"><span data-stu-id="4680f-131">The **magic** member must be set to 0x32484400.</span></span> <span data-ttu-id="4680f-132">Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de « DH2 ».</span><span class="sxs-lookup"><span data-stu-id="4680f-132">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of "DH2".</span></span> |
| <span data-ttu-id="4680f-133">générateur</span><span class="sxs-lookup"><span data-stu-id="4680f-133">generator</span></span>      | <span data-ttu-id="4680f-134">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="4680f-134">A **BYTE** sequence.</span></span> <span data-ttu-id="4680f-135">Générateur, G.</span><span class="sxs-lookup"><span data-stu-id="4680f-135">The generator, G.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="4680f-136">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="4680f-136">publickeystruc</span></span> | <span data-ttu-id="4680f-137">Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="4680f-137">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                        |
| <span data-ttu-id="4680f-138">candidat</span><span class="sxs-lookup"><span data-stu-id="4680f-138">prime</span></span>          | <span data-ttu-id="4680f-139">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="4680f-139">A **BYTE** sequence.</span></span> <span data-ttu-id="4680f-140">Le modulo principal, P. Ces données doivent toujours avoir le bit le plus significatif de l’octet le plus significatif défini sur un.</span><span class="sxs-lookup"><span data-stu-id="4680f-140">The prime modulus, P. This data must always have the most significant bit of the most significant byte set to one.</span></span>                                                                      |
| <span data-ttu-id="4680f-141">secret</span><span class="sxs-lookup"><span data-stu-id="4680f-141">secret</span></span>         | <span data-ttu-id="4680f-142">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="4680f-142">A **BYTE** sequence.</span></span> <span data-ttu-id="4680f-143">Exposant secret, X.</span><span class="sxs-lookup"><span data-stu-id="4680f-143">The secret exponent, X.</span></span>                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="4680f-144">Le générateur et le secret doivent toujours avoir la même longueur, en octets.</span><span class="sxs-lookup"><span data-stu-id="4680f-144">The generator and secret must always have the same length, in bytes.</span></span> <span data-ttu-id="4680f-145">Si l’un ou l’autre octet est plus petit que l’autre, il doit être complété avec le nombre d’octets de zéro valeur nécessaire pour les rendre identiques.</span><span class="sxs-lookup"><span data-stu-id="4680f-145">If either is one byte or more shorter than the other, it must be padded with the necessary number of zero value bytes to make them the same.</span></span> <span data-ttu-id="4680f-146">Le générateur et le secret sont au format [*Little endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4680f-146">Both the generator and the secret are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>

 

 

 
