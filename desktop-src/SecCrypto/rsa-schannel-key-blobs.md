---
description: Les objets BLOB sont utilisés avec le fournisseur RSA/SChannel pour exporter des clés et importer des clés dans, le fournisseur de services de chiffrement (CSP).
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: Objets BLOB de clé RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea26a98e9c2925442166eb28245ebc471b1749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862830"
---
# <a name="rsaschannel-key-blobs"></a><span data-ttu-id="9dfcf-103">Objets BLOB de clé RSA/Schannel</span><span class="sxs-lookup"><span data-stu-id="9dfcf-103">RSA/Schannel Key BLOBs</span></span>

<span data-ttu-id="9dfcf-104">Les [*objets BLOB*](../secgloss/b-gly.md) sont utilisés avec le fournisseur [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) pour exporter les clés et importer les clés dans, le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="9dfcf-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="9dfcf-105">Objets BLOB de clé publique</span><span class="sxs-lookup"><span data-stu-id="9dfcf-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="9dfcf-106">Objets BLOB de clé privée</span><span class="sxs-lookup"><span data-stu-id="9dfcf-106">Private Key BLOBs</span></span>](#private-key-blobs)
-   [<span data-ttu-id="9dfcf-107">Objets BLOB de clé simple</span><span class="sxs-lookup"><span data-stu-id="9dfcf-107">Simple Key BLOBs</span></span>](#simple-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="9dfcf-108">Objets BLOB de clé publique</span><span class="sxs-lookup"><span data-stu-id="9dfcf-108">Public Key BLOBs</span></span>

<span data-ttu-id="9dfcf-109">Les [*objets BLOB de clé publique*](../secgloss/p-gly.md), de type **publicKeyBlob**, sont utilisés pour stocker les [*clés publiques*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9dfcf-109">[*Public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to store [*public keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="9dfcf-110">Ces clés sont exportées et importées sous la forme d’une séquence d’octets au format suivant.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-110">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

<span data-ttu-id="9dfcf-111">Le tableau suivant décrit chaque composant de clé publique.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-111">The following table describes each public key component.</span></span> <span data-ttu-id="9dfcf-112">Toutes les valeurs sont au format [*Little endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-112">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="9dfcf-113">Champ</span><span class="sxs-lookup"><span data-stu-id="9dfcf-113">Field</span></span>          | <span data-ttu-id="9dfcf-114">Description</span><span class="sxs-lookup"><span data-stu-id="9dfcf-114">Description</span></span>                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfcf-115">modulo</span><span class="sxs-lookup"><span data-stu-id="9dfcf-115">modulus</span></span>        | <span data-ttu-id="9dfcf-116">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-116">A **BYTE** sequence.</span></span> <span data-ttu-id="9dfcf-117">Les données du modulo de la clé publique se trouvent directement après la structure **RSAPUBKEY** .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-117">The public key modulus data is located directly after the **RSAPUBKEY** structure.</span></span> <span data-ttu-id="9dfcf-118">La longueur de ces données varie en fonction de la longueur de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-118">The length of this data varies, depending on the length of the public key.</span></span> <span data-ttu-id="9dfcf-119">Le nombre d’octets peut être déterminé en divisant la valeur du membre **bitlen** de **RSAPUBKEY** par huit.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-119">The number of bytes can be determined by dividing the value of the **bitlen** member of **RSAPUBKEY** by eight.</span></span> |
| <span data-ttu-id="9dfcf-120">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="9dfcf-120">publickeystruc</span></span> | <span data-ttu-id="9dfcf-121">Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-121">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="9dfcf-122">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="9dfcf-122">rsapubkey</span></span>      | <span data-ttu-id="9dfcf-123">Structure [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-123">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="9dfcf-124">Le membre **magique** doit être défini sur 0x31415352.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-124">The **magic** member must be set to 0x31415352.</span></span> <span data-ttu-id="9dfcf-125">Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de RSA1.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-125">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA1.</span></span>                                                                                      |



 

> [!Note]  
> <span data-ttu-id="9dfcf-126">Les objets BLOB de clé publique ne sont pas chiffrés.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-126">Public key BLOBs are not encrypted.</span></span> <span data-ttu-id="9dfcf-127">Elles contiennent des clés publiques sous forme de [*texte en clair*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-127">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="9dfcf-128">Objets BLOB de clé privée</span><span class="sxs-lookup"><span data-stu-id="9dfcf-128">Private Key BLOBs</span></span>

<span data-ttu-id="9dfcf-129">Les [*objets BLOB de clé privée*](../secgloss/p-gly.md), de type **PRIVATEKEYBLOB**, sont utilisés pour stocker les [*paires de clés publique/privée*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9dfcf-129">[*Private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store [*public/private key pairs*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="9dfcf-130">Ces clés sont exportées et importées sous la forme d’une séquence d’octets au format suivant.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-130">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
BYTE            prime1[rsapubkey.bitlen/16];
BYTE            prime2[rsapubkey.bitlen/16];
BYTE            exponent1[rsapubkey.bitlen/16];
BYTE            exponent2[rsapubkey.bitlen/16];
BYTE            coefficient[rsapubkey.bitlen/16];
BYTE            privateExponent[rsapubkey.bitlen/8];
```

<span data-ttu-id="9dfcf-131">Si l' [*objet blob de clé*](../secgloss/k-gly.md) est chiffré, tout sauf la partie [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) de l’objet blob est chiffré.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-131">If the [*key BLOB*](../secgloss/k-gly.md) is encrypted, then everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="9dfcf-132">Les paramètres d’algorithme de chiffrement et de clé de chiffrement ne sont pas stockés avec l’objet BLOB de clé privée.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-132">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="9dfcf-133">Il incombe à l’application de gérer ces informations.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-133">It is the responsibility of the application to manage this information.</span></span>

 

<span data-ttu-id="9dfcf-134">Le tableau suivant décrit chaque composant BLOB de clé privée.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-134">The following table describes each private key BLOB component.</span></span>

> [!Note]  
> <span data-ttu-id="9dfcf-135">Ces champs correspondent aux champs décrits dans la section 7,2 des [*normes de chiffrement à clé publique*](../secgloss/p-gly.md) (PKCS) \# 1 avec des différences mineures.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-135">These fields correspond to the fields described in section 7.2 of [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1 with minor differences.</span></span>

 



| <span data-ttu-id="9dfcf-136">Champ</span><span class="sxs-lookup"><span data-stu-id="9dfcf-136">Field</span></span>           | <span data-ttu-id="9dfcf-137">Description</span><span class="sxs-lookup"><span data-stu-id="9dfcf-137">Description</span></span>                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfcf-138">exponent1</span><span class="sxs-lookup"><span data-stu-id="9dfcf-138">exponent1</span></span>       | <span data-ttu-id="9dfcf-139">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-139">A **BYTE** sequence.</span></span> <span data-ttu-id="9dfcf-140">Premier exposant.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-140">The first exponent.</span></span> <span data-ttu-id="9dfcf-141">Il a une valeur numérique de d mod (p – 1).</span><span class="sxs-lookup"><span data-stu-id="9dfcf-141">This has a numeric value of d mod (p – 1).</span></span>                                                                                                                           |
| <span data-ttu-id="9dfcf-142">exponent2</span><span class="sxs-lookup"><span data-stu-id="9dfcf-142">exponent2</span></span>       | <span data-ttu-id="9dfcf-143">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-143">A **BYTE** sequence.</span></span> <span data-ttu-id="9dfcf-144">Deuxième exposant.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-144">The second exponent.</span></span> <span data-ttu-id="9dfcf-145">Il a une valeur numérique de d mod (q – 1).</span><span class="sxs-lookup"><span data-stu-id="9dfcf-145">This has a numeric value of d mod (q – 1).</span></span>                                                                                                                          |
| <span data-ttu-id="9dfcf-146">coefficient</span><span class="sxs-lookup"><span data-stu-id="9dfcf-146">coefficient</span></span>     | <span data-ttu-id="9dfcf-147">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-147">A **BYTE** sequence.</span></span> <span data-ttu-id="9dfcf-148">Coefficient.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-148">Coefficient.</span></span> <span data-ttu-id="9dfcf-149">A la valeur numérique (inverse de q) mod p.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-149">This has a numeric value of (inverse of q) mod p.</span></span>                                                                                                                           |
| <span data-ttu-id="9dfcf-150">Modulus</span><span class="sxs-lookup"><span data-stu-id="9dfcf-150">Modulus</span></span>         | <span data-ttu-id="9dfcf-151">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-151">A **BYTE** sequence.</span></span> <span data-ttu-id="9dfcf-152">Modulo.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-152">The modulus.</span></span> <span data-ttu-id="9dfcf-153">A une chaîne qui contient *Prime1* \* *Prime2*.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-153">This has a string that contains *Prime1* \* *Prime2*.</span></span> <span data-ttu-id="9dfcf-154">Il est souvent appelé n.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-154">It is often known as n.</span></span>                                                                                               |
| <span data-ttu-id="9dfcf-155">prime1</span><span class="sxs-lookup"><span data-stu-id="9dfcf-155">prime1</span></span>          | <span data-ttu-id="9dfcf-156">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-156">A **BYTE** sequence.</span></span> <span data-ttu-id="9dfcf-157">Nombre premier 1, souvent appelé p.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-157">Prime number 1, often known as p.</span></span>                                                                                                                                                        |
| <span data-ttu-id="9dfcf-158">prime2</span><span class="sxs-lookup"><span data-stu-id="9dfcf-158">prime2</span></span>          | <span data-ttu-id="9dfcf-159">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-159">A **BYTE** sequence.</span></span> <span data-ttu-id="9dfcf-160">Nombre premier 2, souvent appelé q.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-160">Prime number 2, often known as q.</span></span>                                                                                                                                                        |
| <span data-ttu-id="9dfcf-161">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="9dfcf-161">publickeystruc</span></span>  | <span data-ttu-id="9dfcf-162">Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-162">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                         |
| <span data-ttu-id="9dfcf-163">privateExponent</span><span class="sxs-lookup"><span data-stu-id="9dfcf-163">privateExponent</span></span> | <span data-ttu-id="9dfcf-164">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-164">A **BYTE** sequence.</span></span> <span data-ttu-id="9dfcf-165">Exposant privé, souvent appelé d.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-165">The private exponent, often known as d.</span></span>                                                                                                                                                  |
| <span data-ttu-id="9dfcf-166">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="9dfcf-166">rsapubkey</span></span>       | <span data-ttu-id="9dfcf-167">Structure [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-167">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="9dfcf-168">Le membre **magique** doit être défini sur 0x32415352.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-168">The **magic** member must be set to 0x32415352.</span></span> <span data-ttu-id="9dfcf-169">Cette valeur hexadécimale est l’encodage [*ASCII*](../secgloss/a-gly.md) de RSA2.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-169">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA2.</span></span> |



 

> [!Note]  
> <span data-ttu-id="9dfcf-170">Les objets BLOB de clé privée ne sont pas chiffrés.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-170">Private key BLOBs are not encrypted.</span></span> <span data-ttu-id="9dfcf-171">Elles contiennent des clés privées sous forme de texte en clair.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-171">They contain private keys in plaintext form.</span></span>

 

<span data-ttu-id="9dfcf-172">Lors de l’appel de [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), le développeur peut choisir de chiffrer ou non la clé.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-172">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="9dfcf-173">Le **PRIVATEKEYBLOB** est chiffré si le paramètre *hExpKey* contient un handle valide pour une clé de session.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-173">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="9dfcf-174">Tout sauf la partie [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) de l’objet blob est chiffré.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-174">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="9dfcf-175">Les paramètres d’algorithme de chiffrement et de clé de chiffrement ne sont pas stockés avec l’objet BLOB de clé privée.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-175">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="9dfcf-176">L’application doit gérer et stocker ces informations.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-176">The application must manage and store this information.</span></span> <span data-ttu-id="9dfcf-177">Si la valeur zéro est passée pour *hExpKey*, la clé privée est exportée sans chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-177">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="9dfcf-178">Il est dangereux d’exporter les clés privées sans chiffrement, car elles sont ensuite vulnérables à l’interception et à l’utilisation par des entités non autorisées.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-178">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

## <a name="simple-key-blobs"></a><span data-ttu-id="9dfcf-179">Objets BLOB de clé simple</span><span class="sxs-lookup"><span data-stu-id="9dfcf-179">Simple Key BLOBs</span></span>

<span data-ttu-id="9dfcf-180">Les [*objets BLOB de clé simple*](../secgloss/s-gly.md), de type **SIMPLEBLOB**, sont utilisés pour stocker et transporter des clés de session.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-180">[*Simple key BLOBs*](../secgloss/s-gly.md), type **SIMPLEBLOB**, are used to store and transport session keys.</span></span> <span data-ttu-id="9dfcf-181">Ils sont toujours chiffrés avec une [*clé publique d’échange de clés*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9dfcf-181">These are always encrypted with a [*key exchange public key*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="9dfcf-182">Ces clés sont exportées et importées sous la forme d’une séquence d’octets au format suivant.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-182">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

<span data-ttu-id="9dfcf-183">Le tableau suivant décrit chaque composant d’objet BLOB simple.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-183">The following table describes each simple BLOB component.</span></span>



| <span data-ttu-id="9dfcf-184">Champ</span><span class="sxs-lookup"><span data-stu-id="9dfcf-184">Field</span></span>          | <span data-ttu-id="9dfcf-185">Description</span><span class="sxs-lookup"><span data-stu-id="9dfcf-185">Description</span></span>                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfcf-186">algid</span><span class="sxs-lookup"><span data-stu-id="9dfcf-186">algid</span></span>          | <span data-ttu-id="9dfcf-187">Structure [**d' \_ ID ALG**](alg-id.md) .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-187">An [**ALG\_ID**](alg-id.md) structure.</span></span> <span data-ttu-id="9dfcf-188">Cela spécifie généralement l' \_ \_ algorithme RSA KEYX CALG, qui indique que les données de la clé de session ont été chiffrées avec une clé publique d’échange de clés, à l’aide de l' [*algorithme de clé publique RSA*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9dfcf-188">This typically specifies the CALG\_RSA\_KEYX algorithm, which indicates that the session key data was encrypted with a key exchange public key, using the [*RSA Public Key algorithm*](../secgloss/r-gly.md).</span></span> |
| <span data-ttu-id="9dfcf-189">EncryptedKey</span><span class="sxs-lookup"><span data-stu-id="9dfcf-189">encryptedkey</span></span>   | <span data-ttu-id="9dfcf-190">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-190">A **BYTE** sequence.</span></span> <span data-ttu-id="9dfcf-191">Les données de la clé de session chiffrée se présente sous la forme d’un \# bloc de chiffrement PKCS 1, type 2.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-191">The encrypted session key data is in the form of a PKCS \#1, type 2 encryption block.</span></span> <span data-ttu-id="9dfcf-192">Pour plus d’informations sur ce format de données, consultez les normes de chiffrement à clé publique (PKCS), publiées par RSA Data Security, Inc.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-192">For information about this data format, see the Public Key Cryptography Standards (PKCS), published by RSA Data Security, Inc.</span></span>                                                                                     |
| <span data-ttu-id="9dfcf-193">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="9dfcf-193">publickeystruc</span></span> | <span data-ttu-id="9dfcf-194">Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="9dfcf-194">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="9dfcf-195">Ces données ont toujours la même taille que le modulo de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-195">This data is always the same size as the modulus of the public key.</span></span> <span data-ttu-id="9dfcf-196">Par exemple, les clés publiques générées par le fournisseur de services de chiffrement de base Microsoft ont toujours une longueur de 512 bits (64 octets). par conséquent, les données de la clé de session chiffrée sont également toujours de 64 octets.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-196">For example, public keys generated by the Microsoft Base Cryptographic Provider are always 512 bits (64 bytes) in length, so the encrypted session key data is also always 64 bytes.</span></span>

 

 
