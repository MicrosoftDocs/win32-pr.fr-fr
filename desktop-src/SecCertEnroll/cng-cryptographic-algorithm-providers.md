---
description: 'Contrairement à l’API de chiffrement (CryptoAPI), API de chiffrement : Next Generation (CNG) sépare les fournisseurs de chiffrement des fournisseurs de stockage de clés.'
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: Fournisseurs d’algorithmes de chiffrement CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc64926236157e581ce6406d95681bd8d4add14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538917"
---
# <a name="cng-cryptographic-algorithm-providers"></a><span data-ttu-id="c70a7-103">Fournisseurs d’algorithmes de chiffrement CNG</span><span class="sxs-lookup"><span data-stu-id="c70a7-103">CNG Cryptographic Algorithm Providers</span></span>

<span data-ttu-id="c70a7-104">Contrairement à l’API de chiffrement (CryptoAPI), API de chiffrement : Next Generation (CNG) sépare les fournisseurs de chiffrement des fournisseurs de stockage de clés.</span><span class="sxs-lookup"><span data-stu-id="c70a7-104">Unlike Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separates cryptographic providers from key storage providers.</span></span> <span data-ttu-id="c70a7-105">Les opérations d’algorithme de chiffrement de base, telles que le hachage et la signature, sont appelées opérations primitives ou simplement Primitives.</span><span class="sxs-lookup"><span data-stu-id="c70a7-105">Basic cryptographic algorithm operations such as hashing and signing are called primitive operations or simply primitives.</span></span> <span data-ttu-id="c70a7-106">CNG intègre un fournisseur qui implémente les algorithmes suivants.</span><span class="sxs-lookup"><span data-stu-id="c70a7-106">CNG includes a provider that implements the following algorithms.</span></span>

-   [<span data-ttu-id="c70a7-107">Algorithmes symétriques</span><span class="sxs-lookup"><span data-stu-id="c70a7-107">Symmetric Algorithms</span></span>](#symmetric-algorithms)
-   [<span data-ttu-id="c70a7-108">Algorithmes asymétriques</span><span class="sxs-lookup"><span data-stu-id="c70a7-108">Asymmetric Algorithms</span></span>](#asymmetric-algorithms)
-   [<span data-ttu-id="c70a7-109">Algorithmes de hachage</span><span class="sxs-lookup"><span data-stu-id="c70a7-109">Hashing Algorithms</span></span>](#hashing-algorithms)
-   [<span data-ttu-id="c70a7-110">Algorithmes d’échange de clés</span><span class="sxs-lookup"><span data-stu-id="c70a7-110">Key Exchange Algorithms</span></span>](#key-exchange-algorithms)
-   [<span data-ttu-id="c70a7-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c70a7-111">Related topics</span></span>](#related-topics)

## <a name="symmetric-algorithms"></a><span data-ttu-id="c70a7-112">Algorithmes symétriques</span><span class="sxs-lookup"><span data-stu-id="c70a7-112">Symmetric Algorithms</span></span>



| <span data-ttu-id="c70a7-113">Nom</span><span class="sxs-lookup"><span data-stu-id="c70a7-113">Name</span></span>                                   | <span data-ttu-id="c70a7-114">Modes pris en charge</span><span class="sxs-lookup"><span data-stu-id="c70a7-114">Supported modes</span></span>                                                                                                                                                                                                 | <span data-ttu-id="c70a7-115">Taille de la clé en bits (valeur par défaut/min/max)</span><span class="sxs-lookup"><span data-stu-id="c70a7-115">Key size in bits (Default/Min/Max)</span></span> |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="c70a7-116">AES (Advanced Encryption Standard)</span><span class="sxs-lookup"><span data-stu-id="c70a7-116">Advanced Encryption Standard (AES)</span></span>     | <span data-ttu-id="c70a7-117">BCE, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, AES Key Wrap, XTS</span><span class="sxs-lookup"><span data-stu-id="c70a7-117">ECB, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, AES Key Wrap, XTS</span></span><br/> <span data-ttu-id="c70a7-118">**Windows 8 :** La prise en charge des modes CFB128 et CMAC démarre.</span><span class="sxs-lookup"><span data-stu-id="c70a7-118">**Windows 8:** Support for the CFB128 and CMAC modes begins.</span></span><br/> <span data-ttu-id="c70a7-119">**Windows 10 :** La prise en charge du mode XTS-AES démarre.</span><span class="sxs-lookup"><span data-stu-id="c70a7-119">**Windows 10:** Support for XTS-AES mode begins.</span></span><br/> | <span data-ttu-id="c70a7-120">128/192/256</span><span class="sxs-lookup"><span data-stu-id="c70a7-120">128/192/256</span></span>                        |
| <span data-ttu-id="c70a7-121">Data Encryption Standard (DES)</span><span class="sxs-lookup"><span data-stu-id="c70a7-121">Data Encryption Standard (DES)</span></span>         | <span data-ttu-id="c70a7-122">BCE, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="c70a7-122">ECB, CBC, CFB8, CFB64</span></span><br/> <span data-ttu-id="c70a7-123">**Windows 8 :** La prise en charge du mode CFB64 commence.</span><span class="sxs-lookup"><span data-stu-id="c70a7-123">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                   | <span data-ttu-id="c70a7-124">56/56/56</span><span class="sxs-lookup"><span data-stu-id="c70a7-124">56/56/56</span></span>                           |
| <span data-ttu-id="c70a7-125">DESX (Data Encryption Standard XOR)</span><span class="sxs-lookup"><span data-stu-id="c70a7-125">Data Encryption Standard XORed(DESX)</span></span>   | <span data-ttu-id="c70a7-126">BCE, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="c70a7-126">ECB, CBC, CFB8, CFB64</span></span> <br/> <span data-ttu-id="c70a7-127">**Windows 8 :** La prise en charge du mode CFB64 commence.</span><span class="sxs-lookup"><span data-stu-id="c70a7-127">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                  | <span data-ttu-id="c70a7-128">192/192/192</span><span class="sxs-lookup"><span data-stu-id="c70a7-128">192/192/192</span></span>                        |
| <span data-ttu-id="c70a7-129">3DES (Triple Data Encryption Standard)</span><span class="sxs-lookup"><span data-stu-id="c70a7-129">Triple Data Encryption Standard (3DES)</span></span> | <span data-ttu-id="c70a7-130">BCE, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="c70a7-130">ECB, CBC, CFB8, CFB64</span></span> <br/> <span data-ttu-id="c70a7-131">**Windows 8 :** La prise en charge du mode CFB64 commence.</span><span class="sxs-lookup"><span data-stu-id="c70a7-131">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                  | <span data-ttu-id="c70a7-132">112/168</span><span class="sxs-lookup"><span data-stu-id="c70a7-132">112/168</span></span>                            |
| <span data-ttu-id="c70a7-133">RSA Data Security 2 (RC2)</span><span class="sxs-lookup"><span data-stu-id="c70a7-133">RSA Data Security 2 (RC2)</span></span>              | <span data-ttu-id="c70a7-134">Les modes ECB, CBC, CFB8 et CFB64 sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c70a7-134">ECB, CBC, CFB8, CFB64 modes are supported.</span></span><br/> <span data-ttu-id="c70a7-135">**Windows 8 :** La prise en charge du mode CFB64 commence.</span><span class="sxs-lookup"><span data-stu-id="c70a7-135">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                              | <span data-ttu-id="c70a7-136">de 16 à 128 par incréments de 8 bits</span><span class="sxs-lookup"><span data-stu-id="c70a7-136">16 to 128 in 8 bit increments</span></span>      |
| <span data-ttu-id="c70a7-137">RSA Data Security 4 (RC4)</span><span class="sxs-lookup"><span data-stu-id="c70a7-137">RSA Data Security 4 (RC4)</span></span>              |                                                                                                                                                                                                                 | <span data-ttu-id="c70a7-138">8 à 512, par incréments de 8 bits</span><span class="sxs-lookup"><span data-stu-id="c70a7-138">8 to 512, in 8-bit increments</span></span>      |



 

## <a name="asymmetric-algorithms"></a><span data-ttu-id="c70a7-139">Algorithmes asymétriques</span><span class="sxs-lookup"><span data-stu-id="c70a7-139">Asymmetric Algorithms</span></span>



| <span data-ttu-id="c70a7-140">Nom</span><span class="sxs-lookup"><span data-stu-id="c70a7-140">Name</span></span>                              | <span data-ttu-id="c70a7-141">Notes</span><span class="sxs-lookup"><span data-stu-id="c70a7-141">Notes</span></span>                                                                                                                                                                             | <span data-ttu-id="c70a7-142">Taille de la clé en bits (valeur par défaut/min/max)</span><span class="sxs-lookup"><span data-stu-id="c70a7-142">Key size in bits (Default/Min/Max)</span></span>                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c70a7-143">Algorithme de signature numérique (DSA)</span><span class="sxs-lookup"><span data-stu-id="c70a7-143">Digital Signature Algorithm (DSA)</span></span> | <span data-ttu-id="c70a7-144">L’implémentation est conforme à la norme FIPS 186-3 pour les tailles de clé comprises entre 1024 et 3072 bits.</span><span class="sxs-lookup"><span data-stu-id="c70a7-144">Implementation conforms to FIPS 186-3 for key sizes between 1024 and 3072 bits.</span></span> <br/> <span data-ttu-id="c70a7-145">L’implémentation est conforme à la norme FIPS 186-2 pour les tailles de clé de 512 à 1024 bits.</span><span class="sxs-lookup"><span data-stu-id="c70a7-145">Implementation conforms to FIPS 186-2 for key sizes from 512 to 1024 bits.</span></span><br/> | <span data-ttu-id="c70a7-146">512 à 3072, en incréments de 64 bits</span><span class="sxs-lookup"><span data-stu-id="c70a7-146">512 to 3072, in 64-bit increments</span></span><br/> <span data-ttu-id="c70a7-147">**Windows 8 :** La prise en charge de la clé a 3072 bits commence.</span><span class="sxs-lookup"><span data-stu-id="c70a7-147">**Windows 8:** Support for the a 3072 bit key begins.</span></span><br/> |
| <span data-ttu-id="c70a7-148">RSA</span><span class="sxs-lookup"><span data-stu-id="c70a7-148">RSA</span></span>                               | <span data-ttu-id="c70a7-149">Comprend des algorithmes RSA qui utilisent PKCS1, l’encodage ou le remplissage OAEP (Optimal Asymmetric Encryption Padding) ou le remplissage en texte clair du schéma de signature probabiliste (PSS).</span><span class="sxs-lookup"><span data-stu-id="c70a7-149">Includes RSA algorithms that use PKCS1, Optimal Asymmetric Encryption Padding (OAEP) encoding or padding, or Probabilistic Signature Scheme (PSS) plaintext padding</span></span>               | <span data-ttu-id="c70a7-150">512 à 16384, en incréments de 64 bits</span><span class="sxs-lookup"><span data-stu-id="c70a7-150">512 to 16384, in 64-bit increments</span></span>                                                                            |



 

## <a name="hashing-algorithms"></a><span data-ttu-id="c70a7-151">Algorithmes de hachage</span><span class="sxs-lookup"><span data-stu-id="c70a7-151">Hashing Algorithms</span></span>



| <span data-ttu-id="c70a7-152">Nom</span><span class="sxs-lookup"><span data-stu-id="c70a7-152">Name</span></span>                               | <span data-ttu-id="c70a7-153">Notes</span><span class="sxs-lookup"><span data-stu-id="c70a7-153">Notes</span></span>               | <span data-ttu-id="c70a7-154">Taille de la clé en bits (valeur par défaut/min/max)</span><span class="sxs-lookup"><span data-stu-id="c70a7-154">Key size in bits (Default/Min/Max)</span></span> |
|------------------------------------|---------------------|------------------------------------|
| <span data-ttu-id="c70a7-155">Secure Hash Algorithm 1 (SHA1)</span><span class="sxs-lookup"><span data-stu-id="c70a7-155">Secure Hash Algorithm 1 (SHA1)</span></span>     | <span data-ttu-id="c70a7-156">Comprend HmacSha1</span><span class="sxs-lookup"><span data-stu-id="c70a7-156">Includes HmacSha1</span></span>   | <span data-ttu-id="c70a7-157">160/160/160</span><span class="sxs-lookup"><span data-stu-id="c70a7-157">160/160/160</span></span>                        |
| <span data-ttu-id="c70a7-158">Algorithme de hachage sécurisé 256 (SHA256)</span><span class="sxs-lookup"><span data-stu-id="c70a7-158">Secure Hash Algorithm 256 (SHA256)</span></span> | <span data-ttu-id="c70a7-159">Comprend HmacSha256</span><span class="sxs-lookup"><span data-stu-id="c70a7-159">Includes HmacSha256</span></span> | <span data-ttu-id="c70a7-160">256/256/256</span><span class="sxs-lookup"><span data-stu-id="c70a7-160">256/256/256</span></span>                        |
| <span data-ttu-id="c70a7-161">Algorithme de hachage sécurisé 384 (SHA384)</span><span class="sxs-lookup"><span data-stu-id="c70a7-161">Secure Hash Algorithm 384 (SHA384)</span></span> | <span data-ttu-id="c70a7-162">Comprend HmacSha384</span><span class="sxs-lookup"><span data-stu-id="c70a7-162">Includes HmacSha384</span></span> | <span data-ttu-id="c70a7-163">384/384/384</span><span class="sxs-lookup"><span data-stu-id="c70a7-163">384/384/384</span></span>                        |
| <span data-ttu-id="c70a7-164">Algorithme de hachage sécurisé 512 (SHA512)</span><span class="sxs-lookup"><span data-stu-id="c70a7-164">Secure Hash Algorithm 512 (SHA512)</span></span> | <span data-ttu-id="c70a7-165">Comprend HmacSha512</span><span class="sxs-lookup"><span data-stu-id="c70a7-165">Includes HmacSha512</span></span> | <span data-ttu-id="c70a7-166">512/512/512</span><span class="sxs-lookup"><span data-stu-id="c70a7-166">512/512/512</span></span>                        |
| <span data-ttu-id="c70a7-167">Message condensé 2 (MD2)</span><span class="sxs-lookup"><span data-stu-id="c70a7-167">Message Digest 2 (MD2)</span></span>             | <span data-ttu-id="c70a7-168">Comprend HmacMd2</span><span class="sxs-lookup"><span data-stu-id="c70a7-168">Includes HmacMd2</span></span>    | <span data-ttu-id="c70a7-169">128/128/128</span><span class="sxs-lookup"><span data-stu-id="c70a7-169">128/128/128</span></span>                        |
| <span data-ttu-id="c70a7-170">Message condensé 4 (MD4)</span><span class="sxs-lookup"><span data-stu-id="c70a7-170">Message Digest 4 (MD4)</span></span>             | <span data-ttu-id="c70a7-171">Comprend HmacMd4</span><span class="sxs-lookup"><span data-stu-id="c70a7-171">Includes HmacMd4</span></span>    | <span data-ttu-id="c70a7-172">128/128/128</span><span class="sxs-lookup"><span data-stu-id="c70a7-172">128/128/128</span></span>                        |
| <span data-ttu-id="c70a7-173">Message Digest 5 (MD5)</span><span class="sxs-lookup"><span data-stu-id="c70a7-173">Message Digest 5 (MD5)</span></span>             | <span data-ttu-id="c70a7-174">Comprend HmacMd5</span><span class="sxs-lookup"><span data-stu-id="c70a7-174">Includes HmacMd5</span></span>    | <span data-ttu-id="c70a7-175">128/128/128</span><span class="sxs-lookup"><span data-stu-id="c70a7-175">128/128/128</span></span>                        |



 

## <a name="key-exchange-algorithms"></a><span data-ttu-id="c70a7-176">Algorithmes d’échange de clés</span><span class="sxs-lookup"><span data-stu-id="c70a7-176">Key Exchange Algorithms</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c70a7-177">Nom de l'algorithme</span><span class="sxs-lookup"><span data-stu-id="c70a7-177">Algorithm name</span></span></th>
<th><span data-ttu-id="c70a7-178">Notes</span><span class="sxs-lookup"><span data-stu-id="c70a7-178">Notes</span></span></th>
<th><span data-ttu-id="c70a7-179">Taille de la clé en bits (valeur par défaut/min/max)</span><span class="sxs-lookup"><span data-stu-id="c70a7-179">Key size in bits (Default/Min/Max)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c70a7-180">Algorithme d’échange de clés Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="c70a7-180">Diffie-Hellman Key Exchange Algorithm</span></span></td>

<td><span data-ttu-id="c70a7-181">512 à 4096, en incréments de 64 bits</span><span class="sxs-lookup"><span data-stu-id="c70a7-181">512 to 4096, in 64-bit increments</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c70a7-182">ECDH (Elliptic Curve Diffie-Hellman)</span><span class="sxs-lookup"><span data-stu-id="c70a7-182">Elliptic Curve Diffie-Hellman (ECDH)</span></span></td>
<td><span data-ttu-id="c70a7-183">Comprend des courbes qui utilisent des clés publiques 256, 384 et 521 bits comme spécifié dans SP800-56A.</span><span class="sxs-lookup"><span data-stu-id="c70a7-183">Includes curves that use 256, 384 and 521 bit public keys as specified in SP800-56A.</span></span></td>
<td><span data-ttu-id="c70a7-184">256/384/521</span><span class="sxs-lookup"><span data-stu-id="c70a7-184">256/384/521</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c70a7-185">Algorithme ECDSA (Elliptic Curve Digital Signature Algorithm)</span><span class="sxs-lookup"><span data-stu-id="c70a7-185">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span></td>
<td><span data-ttu-id="c70a7-186">Comprend des courbes qui utilisent des clés publiques 256, 384 et 521 bits comme spécifié dans la norme FIPS 186-3.</span><span class="sxs-lookup"><span data-stu-id="c70a7-186">Includes curves that use 256, 384 and 521 bit public keys as specified in FIPS 186-3.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c70a7-187">Pour afficher toutes les courbes elliptiques nommées, utilisez <strong>certutil displayEccCurve</strong>.</span><span class="sxs-lookup"><span data-stu-id="c70a7-187">To display all named elliptic curves, use <strong>certutil  displayEccCurve</strong>.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="c70a7-188">256/384/521</span><span class="sxs-lookup"><span data-stu-id="c70a7-188">256/384/521</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c70a7-189">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c70a7-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c70a7-190">**Identificateurs d’algorithme CNG**</span><span class="sxs-lookup"><span data-stu-id="c70a7-190">**CNG Algorithm Identifiers**</span></span>](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[<span data-ttu-id="c70a7-191">Fonctions de primitives de chiffrement CNG</span><span class="sxs-lookup"><span data-stu-id="c70a7-191">CNG Cryptographic Primitive Functions</span></span>](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[<span data-ttu-id="c70a7-192">Comprendre les fournisseurs de services de chiffrement</span><span class="sxs-lookup"><span data-stu-id="c70a7-192">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 

