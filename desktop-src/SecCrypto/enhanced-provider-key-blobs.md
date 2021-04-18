---
description: Le fournisseur de base, le fournisseur fort et le fournisseur amélioré utilisent les mêmes objets BLOB de clé.
ms.assetid: f1bd347b-33bd-40bc-9a9b-c06f264f1af4
title: Objets BLOB de clé de fournisseur améliorée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f693fd469a1df2e76078e61bb69c90ea5d5041d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536554"
---
# <a name="enhanced-provider-key-blobs"></a><span data-ttu-id="fd1dc-103">Objets BLOB de clé de fournisseur améliorée</span><span class="sxs-lookup"><span data-stu-id="fd1dc-103">Enhanced Provider Key BLOBs</span></span>

<span data-ttu-id="fd1dc-104">Le fournisseur de base, le fournisseur fort et le fournisseur amélioré utilisent les mêmes [*objets BLOB de clé*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fd1dc-104">The Base Provider, Strong Provider, and Enhanced Provider use the same [*key BLOBs*](../secgloss/k-gly.md).</span></span>

-   [<span data-ttu-id="fd1dc-105">Objets BLOB de clé publique</span><span class="sxs-lookup"><span data-stu-id="fd1dc-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="fd1dc-106">Objets BLOB de clé privée</span><span class="sxs-lookup"><span data-stu-id="fd1dc-106">Private Key BLOBs</span></span>](#private-key-blobs)
-   [<span data-ttu-id="fd1dc-107">Objets BLOB de clé simple</span><span class="sxs-lookup"><span data-stu-id="fd1dc-107">Simple Key BLOBs</span></span>](#simple-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="fd1dc-108">Objets BLOB de clé publique</span><span class="sxs-lookup"><span data-stu-id="fd1dc-108">Public Key BLOBs</span></span>

<span data-ttu-id="fd1dc-109">Les [*objets BLOB de clé publique*](../secgloss/p-gly.md), de type **publicKeyBlob**, sont utilisés pour stocker des [*clés publiques*](../secgloss/p-gly.md) en dehors d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="fd1dc-109">[*Public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to store [*public keys*](../secgloss/p-gly.md) outside a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span> <span data-ttu-id="fd1dc-110">Les objets BLOB de clé publique de fournisseur étendu ont le format suivant.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-110">Extended provider public key BLOBs have the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

<span data-ttu-id="fd1dc-111">Le tableau suivant décrit chaque composant de clé publique.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-111">The following table describes each public key component.</span></span> <span data-ttu-id="fd1dc-112">Toutes les valeurs sont au format [*Little endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="fd1dc-112">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="fd1dc-113">Champ</span><span class="sxs-lookup"><span data-stu-id="fd1dc-113">Field</span></span>          | <span data-ttu-id="fd1dc-114">Description</span><span class="sxs-lookup"><span data-stu-id="fd1dc-114">Description</span></span>                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd1dc-115">modulo</span><span class="sxs-lookup"><span data-stu-id="fd1dc-115">modulus</span></span>        | <span data-ttu-id="fd1dc-116">Les données du modulo de la clé publique se trouvent directement après la structure [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="fd1dc-116">The public key modulus data is located directly after the [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="fd1dc-117">La taille de ces données varie en fonction de la taille de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-117">The size of this data will vary, depending on the size of the public key.</span></span> <span data-ttu-id="fd1dc-118">Le nombre d’octets peut être déterminé en divisant la valeur du champ **RSAPUBKEY bitlen** par huit.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-118">The number of bytes can be determined by dividing the value of the **RSAPUBKEY bitlen** field by eight.</span></span> |
| <span data-ttu-id="fd1dc-119">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="fd1dc-119">publickeystruc</span></span> | <span data-ttu-id="fd1dc-120">Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="fd1dc-120">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="fd1dc-121">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="fd1dc-121">rsapubkey</span></span>      | <span data-ttu-id="fd1dc-122">Structure [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="fd1dc-122">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="fd1dc-123">Le membre **magique** doit être défini sur 0x31415352.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-123">The **magic** member must be set to 0x31415352.</span></span> <span data-ttu-id="fd1dc-124">Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de RSA1.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-124">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA1.</span></span>                                                                         |



 

> [!Note]  
> <span data-ttu-id="fd1dc-125">Les objets BLOB de clé publique ne sont pas chiffrés.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-125">Public key BLOBs are not encrypted.</span></span> <span data-ttu-id="fd1dc-126">Elles contiennent des clés publiques sous forme de [*texte en clair*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="fd1dc-126">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="fd1dc-127">Objets BLOB de clé privée</span><span class="sxs-lookup"><span data-stu-id="fd1dc-127">Private Key BLOBs</span></span>

<span data-ttu-id="fd1dc-128">Les [*objets BLOB de clé privée*](../secgloss/p-gly.md), de type **PRIVATEKEYBLOB**, sont utilisés pour stocker des [*clés privées*](../secgloss/p-gly.md) en dehors d’un CSP.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-128">[*Private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store [*private keys*](../secgloss/p-gly.md) outside a CSP.</span></span> <span data-ttu-id="fd1dc-129">Les objets BLOB de clé privée du fournisseur étendu ont le format suivant.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-129">Extended provider private key BLOBs have the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
BYTE prime1[rsapubkey.bitlen/16];
BYTE prime2[rsapubkey.bitlen/16];
BYTE exponent1[rsapubkey.bitlen/16];
BYTE exponent2[rsapubkey.bitlen/16];
BYTE coefficient[rsapubkey.bitlen/16];
BYTE privateExponent[rsapubkey.bitlen/8];
```

<span data-ttu-id="fd1dc-130">Le tableau suivant décrit le composant BLOB de clé privée.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-130">The following table describes the private key BLOB component.</span></span>

> [!Note]  
> <span data-ttu-id="fd1dc-131">Ces champs correspondent aux champs décrits dans la section 7,2 des [*normes de chiffrement à clé publique*](../secgloss/p-gly.md) (PKCS) \# 1 avec des différences mineures.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-131">These fields correspond to the fields described in section 7.2 of [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1 with minor differences.</span></span>

 



| <span data-ttu-id="fd1dc-132">Champ</span><span class="sxs-lookup"><span data-stu-id="fd1dc-132">Field</span></span>           | <span data-ttu-id="fd1dc-133">Description</span><span class="sxs-lookup"><span data-stu-id="fd1dc-133">Description</span></span>                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd1dc-134">coefficient</span><span class="sxs-lookup"><span data-stu-id="fd1dc-134">coefficient</span></span>     | <span data-ttu-id="fd1dc-135">Coefficient.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-135">Coefficient.</span></span> <span data-ttu-id="fd1dc-136">A la valeur numérique (inverse de q) mod p.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-136">This has a numeric value of (inverse of q) mod p.</span></span>                                                                                                                                                |
| <span data-ttu-id="fd1dc-137">exponent1</span><span class="sxs-lookup"><span data-stu-id="fd1dc-137">exponent1</span></span>       | <span data-ttu-id="fd1dc-138">Exposant 1.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-138">Exponent 1.</span></span> <span data-ttu-id="fd1dc-139">Il a une valeur numérique de d mod (p – 1).</span><span class="sxs-lookup"><span data-stu-id="fd1dc-139">This has a numeric value of d mod (p – 1).</span></span>                                                                                                                                                        |
| <span data-ttu-id="fd1dc-140">exponent2</span><span class="sxs-lookup"><span data-stu-id="fd1dc-140">exponent2</span></span>       | <span data-ttu-id="fd1dc-141">Exposant 2.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-141">Exponent 2.</span></span> <span data-ttu-id="fd1dc-142">Il a une valeur numérique de d mod (q – 1).</span><span class="sxs-lookup"><span data-stu-id="fd1dc-142">This has a numeric value of d mod (q – 1).</span></span>                                                                                                                                                        |
| <span data-ttu-id="fd1dc-143">Modulus</span><span class="sxs-lookup"><span data-stu-id="fd1dc-143">Modulus</span></span>         | <span data-ttu-id="fd1dc-144">Modulo.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-144">The modulus.</span></span> <span data-ttu-id="fd1dc-145">Il a la valeur *Prime1*×*Prime2* et est souvent appelé n.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-145">This has a value of *Prime1*×*Prime2* and is often known as n.</span></span>                                                                                                                                   |
| <span data-ttu-id="fd1dc-146">prime1</span><span class="sxs-lookup"><span data-stu-id="fd1dc-146">prime1</span></span>          | <span data-ttu-id="fd1dc-147">Nombre premier 1, souvent appelé p.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-147">Prime number 1, often known as p.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="fd1dc-148">prime2</span><span class="sxs-lookup"><span data-stu-id="fd1dc-148">prime2</span></span>          | <span data-ttu-id="fd1dc-149">Nombre premier 2, souvent appelé q.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-149">Prime number 2, often known as q.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="fd1dc-150">privateExponent</span><span class="sxs-lookup"><span data-stu-id="fd1dc-150">privateExponent</span></span> | <span data-ttu-id="fd1dc-151">Exposant privé, souvent appelé d.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-151">Private exponent, often known as d.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="fd1dc-152">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="fd1dc-152">publickeystruc</span></span>  | <span data-ttu-id="fd1dc-153">Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="fd1dc-153">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                         |
| <span data-ttu-id="fd1dc-154">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="fd1dc-154">rsapubkey</span></span>       | <span data-ttu-id="fd1dc-155">Structure [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="fd1dc-155">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="fd1dc-156">Le membre **magique** doit être défini sur 0x32415352.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-156">The **magic** member must be set to 0x32415352.</span></span> <span data-ttu-id="fd1dc-157">Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de RSA2.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-157">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA2.</span></span> |



 

> [!Note]  
> <span data-ttu-id="fd1dc-158">Les objets BLOB de clé privée ne sont pas chiffrés.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-158">Private key BLOBs are not encrypted.</span></span> <span data-ttu-id="fd1dc-159">Elles contiennent des clés privées sous forme de texte en clair.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-159">They contain private keys in plaintext form.</span></span>

 

<span data-ttu-id="fd1dc-160">Lors de l’appel de [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), le développeur peut choisir de chiffrer ou non la clé.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-160">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="fd1dc-161">Le **PRIVATEKEYBLOB** est chiffré si le paramètre *hExpKey* contient un handle valide pour une clé de session.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-161">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="fd1dc-162">Tout sauf la partie [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) de l’objet blob est chiffré.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-162">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="fd1dc-163">Les paramètres d’algorithme de chiffrement et de clé de chiffrement ne sont pas stockés avec l’objet BLOB de clé privée.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-163">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="fd1dc-164">L’application doit gérer et stocker ces informations.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-164">The application must manage and store this information.</span></span> <span data-ttu-id="fd1dc-165">Si la valeur zéro est passée pour *hExpKey*, la clé privée est exportée sans chiffrement.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-165">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="fd1dc-166">Il est dangereux d’exporter les clés privées sans chiffrement, car elles sont ensuite vulnérables à l’interception et à l’utilisation par des entités non autorisées.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-166">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

## <a name="simple-key-blobs"></a><span data-ttu-id="fd1dc-167">Objets BLOB de clé simple</span><span class="sxs-lookup"><span data-stu-id="fd1dc-167">Simple Key BLOBs</span></span>

<span data-ttu-id="fd1dc-168">Les [*objets BLOB de clé simple*](../secgloss/s-gly.md), de type **SIMPLEBLOB**, sont utilisés pour stocker et transporter des clés de session en dehors d’un CSP.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-168">[*Simple key BLOBs*](../secgloss/s-gly.md), type **SIMPLEBLOB**, are used to store and transport session keys outside a CSP.</span></span> <span data-ttu-id="fd1dc-169">Les objets BLOB de clé simple du fournisseur étendu sont toujours chiffrés avec une [*clé publique d’échange de clés*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fd1dc-169">Extended provider simple key BLOBs are always encrypted with a [*key exchange public key*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="fd1dc-170">Le membre **pbData** du **SIMPLEBLOB** est une séquence d’octets au format suivant.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-170">The **pbData** member of the **SIMPLEBLOB** is a sequence of bytes in the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

<span data-ttu-id="fd1dc-171">Le tableau suivant décrit chaque composant du membre **pbData** du **SIMPLEBLOB**.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-171">The following table describes each component of the **pbData** member of the **SIMPLEBLOB**.</span></span>



| <span data-ttu-id="fd1dc-172">Champ</span><span class="sxs-lookup"><span data-stu-id="fd1dc-172">Field</span></span>          | <span data-ttu-id="fd1dc-173">Description</span><span class="sxs-lookup"><span data-stu-id="fd1dc-173">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd1dc-174">algid</span><span class="sxs-lookup"><span data-stu-id="fd1dc-174">algid</span></span>          | <span data-ttu-id="fd1dc-175">Structure [**d' \_ ID ALG**](alg-id.md) qui spécifie l’algorithme de chiffrement utilisé pour chiffrer les données de la clé de session.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-175">An [**ALG\_ID**](alg-id.md) structure that specifies the encryption algorithm used to encrypt the session key data.</span></span> <span data-ttu-id="fd1dc-176">Cela a généralement la valeur CALG \_ RSA \_ KEYX, qui indique que les données de la clé de session ont été chiffrées avec une clé publique d’échange de clés à l’aide de l' [*algorithme de clé publique RSA*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fd1dc-176">This typically has a value of CALG\_RSA\_KEYX, which indicates that the session key data was encrypted with a key exchange public key using the [*RSA Public Key algorithm*](../secgloss/r-gly.md).</span></span>                                                                                                                           |
| <span data-ttu-id="fd1dc-177">EncryptedKey</span><span class="sxs-lookup"><span data-stu-id="fd1dc-177">encryptedkey</span></span>   | <span data-ttu-id="fd1dc-178">Séquence d' **octets** qui représente les données de clé de session chiffrées sous la forme d’un \# bloc de chiffrement PKCS 1, type 2.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-178">A **BYTE** sequence that represents the encrypted session key data in the form of a PKCS \#1, type 2 encryption block.</span></span> <span data-ttu-id="fd1dc-179">Pour plus d’informations sur ce format de données, consultez les normes de chiffrement à clé publique (PKCS) \# 1, publiées par RSA Data Security, Inc. Ces données ont toujours la même taille que le modulo de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="fd1dc-179">For information about this data format, see the Public Key Cryptography Standards (PKCS) \#1, published by RSA Data Security, Inc. This data is always the same size as the modulus of the public key.</span></span> <span data-ttu-id="fd1dc-180">Par exemple, les clés publiques générées par le fournisseur de base Microsoft RSA peuvent avoir une longueur de 512 bits (64 octets). par conséquent, les données de clé de session chiffrées sont également toujours 512 bits (64 octets).</span><span class="sxs-lookup"><span data-stu-id="fd1dc-180">For example, public keys generated by the Microsoft RSA Base Provider can be 512 bits (64 bytes) in length, so the encrypted session key data is also always 512 bits (64 bytes).</span></span><br/> |
| <span data-ttu-id="fd1dc-181">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="fd1dc-181">publickeystruc</span></span> | <span data-ttu-id="fd1dc-182">Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="fd1dc-182">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

<span data-ttu-id="fd1dc-183">Pour plus d’informations sur le fournisseur de base et les objets BLOB de clé du fournisseur étendu, consultez [objets BLOB de clé du fournisseur](base-provider-key-blobs.md).</span><span class="sxs-lookup"><span data-stu-id="fd1dc-183">For information about the Base Provider and Extended Provider key BLOBs, see [Base Provider Key BLOBs](base-provider-key-blobs.md).</span></span>

 

 
