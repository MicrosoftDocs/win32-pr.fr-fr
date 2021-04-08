---
description: Les objets BLOB sont utilisés avec le fournisseur Diffie-Hellman/Schannel pour exporter des clés et importer des clés dans, le fournisseur de services de chiffrement (CSP).
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: Objets BLOB de clé Diffie-Hellman/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a76869c6c6239e17a5ae14921805a076c9381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756537"
---
# <a name="diffie-hellmanschannel-key-blobs"></a><span data-ttu-id="9af91-103">Objets BLOB de clé Diffie-Hellman/Schannel</span><span class="sxs-lookup"><span data-stu-id="9af91-103">Diffie-Hellman/Schannel Key BLOBs</span></span>

<span data-ttu-id="9af91-104">Les [*objets BLOB*](../secgloss/b-gly.md) sont utilisés avec le fournisseur Schannel [*Diffie-Hellman*](../secgloss/d-gly.md) / [](../secgloss/s-gly.md) pour exporter des clés et importer des clés dans, le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="9af91-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Diffie-Hellman*](../secgloss/d-gly.md)/[*Schannel*](../secgloss/s-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="9af91-105">Objets BLOB de clé publique</span><span class="sxs-lookup"><span data-stu-id="9af91-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="9af91-106">Objets BLOB de clé privée</span><span class="sxs-lookup"><span data-stu-id="9af91-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="9af91-107">Objets BLOB de clé publique</span><span class="sxs-lookup"><span data-stu-id="9af91-107">Public Key BLOBs</span></span>

<span data-ttu-id="9af91-108">Diffie-Hellman [*objets BLOB de clé publique*](../secgloss/p-gly.md), de type **publicKeyBlob**, sont utilisés pour échanger la valeur (G ^ X) mod P dans un échange de clés Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="9af91-108">Diffie-Hellman [*public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to exchange the (G^X) mod P value in a Diffie-Hellman key exchange.</span></span> <span data-ttu-id="9af91-109">Ces clés sont exportées et importées sous la forme d’une séquence d’octets au format suivant.</span><span class="sxs-lookup"><span data-stu-id="9af91-109">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

<span data-ttu-id="9af91-110">Le tableau suivant décrit chaque composant de l' [*objet blob de clé*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9af91-110">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="9af91-111">Champ</span><span class="sxs-lookup"><span data-stu-id="9af91-111">Field</span></span>          | <span data-ttu-id="9af91-112">Description</span><span class="sxs-lookup"><span data-stu-id="9af91-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af91-113">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="9af91-113">dhpubkey</span></span>       | <span data-ttu-id="9af91-114">Structure [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="9af91-114">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="9af91-115">Le membre **magique** doit être défini sur 0x31484400.</span><span class="sxs-lookup"><span data-stu-id="9af91-115">The **magic** member must be set to 0x31484400.</span></span> <span data-ttu-id="9af91-116">Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de DH1.</span><span class="sxs-lookup"><span data-stu-id="9af91-116">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of DH1.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="9af91-117">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="9af91-117">publickeystruc</span></span> | <span data-ttu-id="9af91-118">Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="9af91-118">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9af91-119">y</span><span class="sxs-lookup"><span data-stu-id="9af91-119">y</span></span>              | <span data-ttu-id="9af91-120">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="9af91-120">A **BYTE** sequence.</span></span> <span data-ttu-id="9af91-121">La valeur y, (G ^ X) mod P, est située directement après la structure [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="9af91-121">The y value, (G^X) mod P, is located directly after the [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="9af91-122">La longueur, en octets, de la séquence est le membre **bitlen** de **DHPUBKEY** divisé par huit.</span><span class="sxs-lookup"><span data-stu-id="9af91-122">The length, in bytes, of the sequence is the **bitlen** member of **DHPUBKEY** divided by eight.</span></span> <span data-ttu-id="9af91-123">Si la longueur des données résultant du calcul de (G ^ X) mod P est un ou plusieurs octets plus courts que P divisés par huit, les données doivent être complétées par les octets nécessaires (de zéro valeur) pour que les données soient de la longueur souhaitée (format [*Little endian*](../secgloss/l-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="9af91-123">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by eight, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |



 

## <a name="private-key-blobs"></a><span data-ttu-id="9af91-124">Objets BLOB de clé privée</span><span class="sxs-lookup"><span data-stu-id="9af91-124">Private Key BLOBs</span></span>

<span data-ttu-id="9af91-125">Les [*objets BLOB de clé privée*](../secgloss/p-gly.md)D-h, de type **PRIVATEKEYBLOB**, sont utilisés pour exporter et importer des informations privées d’une clé D-H.</span><span class="sxs-lookup"><span data-stu-id="9af91-125">D-H [*private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to export and import private information of a D-H key.</span></span> <span data-ttu-id="9af91-126">Ces clés sont exportées et importées sous la forme d’une séquence d’octets au format suivant.</span><span class="sxs-lookup"><span data-stu-id="9af91-126">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

<span data-ttu-id="9af91-127">Le tableau suivant décrit chaque composant de l’objet BLOB de clé.</span><span class="sxs-lookup"><span data-stu-id="9af91-127">The following table describes each component of the key BLOB.</span></span>



| <span data-ttu-id="9af91-128">Champ</span><span class="sxs-lookup"><span data-stu-id="9af91-128">Field</span></span>          | <span data-ttu-id="9af91-129">Description</span><span class="sxs-lookup"><span data-stu-id="9af91-129">Description</span></span>                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af91-130">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="9af91-130">dhpubkey</span></span>       | <span data-ttu-id="9af91-131">Structure [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="9af91-131">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="9af91-132">Le membre **magique** doit être défini sur 0x32484400.</span><span class="sxs-lookup"><span data-stu-id="9af91-132">The **magic** member must be set to 0x32484400.</span></span> <span data-ttu-id="9af91-133">Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de DH2.</span><span class="sxs-lookup"><span data-stu-id="9af91-133">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of DH2.</span></span> |
| <span data-ttu-id="9af91-134">générateur</span><span class="sxs-lookup"><span data-stu-id="9af91-134">generator</span></span>      | <span data-ttu-id="9af91-135">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="9af91-135">A **BYTE** sequence.</span></span> <span data-ttu-id="9af91-136">Générateur G.</span><span class="sxs-lookup"><span data-stu-id="9af91-136">The generator G.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="9af91-137">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="9af91-137">publickeystruc</span></span> | <span data-ttu-id="9af91-138">Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="9af91-138">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                      |
| <span data-ttu-id="9af91-139">candidat</span><span class="sxs-lookup"><span data-stu-id="9af91-139">prime</span></span>          | <span data-ttu-id="9af91-140">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="9af91-140">A **BYTE** sequence.</span></span> <span data-ttu-id="9af91-141">Le modulo principal, P. Ces données doivent toujours avoir le bit le plus significatif de l’octet le plus significatif défini sur un.</span><span class="sxs-lookup"><span data-stu-id="9af91-141">The prime modulus, P. This data must always have the most significant bit of the most significant byte set to one.</span></span>                                                                    |
| <span data-ttu-id="9af91-142">secret</span><span class="sxs-lookup"><span data-stu-id="9af91-142">secret</span></span>         | <span data-ttu-id="9af91-143">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="9af91-143">A **BYTE** sequence.</span></span> <span data-ttu-id="9af91-144">Exposant X secret.</span><span class="sxs-lookup"><span data-stu-id="9af91-144">The secret exponent X.</span></span>                                                                                                                                                                |



 

> [!Note]  
> <span data-ttu-id="9af91-145">Les valeurs prime, générateur et secret doivent toujours avoir la même longueur, en octets.</span><span class="sxs-lookup"><span data-stu-id="9af91-145">The prime, generator, and secret values must always have the same length, in bytes.</span></span> <span data-ttu-id="9af91-146">Si une valeur est d’un octet ou plus, elle doit être complétée avec le nombre de zéro octet nécessaire pour les rendre identiques.</span><span class="sxs-lookup"><span data-stu-id="9af91-146">If any value is one byte or more shorter than the others, it must be padded with the necessary number of zero bytes to make them the same.</span></span> <span data-ttu-id="9af91-147">Le premier, le générateur et le secret sont au format [*Little endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9af91-147">The prime, generator, and secret are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>

 

 

 
