---
description: Spécifie un identificateur d’algorithme.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab1eb6dc262faae76d38f2b96c9e6191a313390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538724"
---
# <a name="alg_id"></a><span data-ttu-id="11013-103">ALG_ID</span><span class="sxs-lookup"><span data-stu-id="11013-103">ALG_ID</span></span>

<span data-ttu-id="11013-104">Le type de données **ALG_ID** spécifie un identificateur d’algorithme.</span><span class="sxs-lookup"><span data-stu-id="11013-104">The **ALG_ID** data type specifies an algorithm identifier.</span></span> <span data-ttu-id="11013-105">Les paramètres de ce type de données sont passés à la plupart des fonctions dans CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="11013-105">Parameters of this data type are passed to most of the functions in CryptoAPI.</span></span>


```C++
typedef unsigned int ALG_ID;
```



<span data-ttu-id="11013-106">Le tableau suivant répertorie les identificateurs d’algorithme actuellement définis.</span><span class="sxs-lookup"><span data-stu-id="11013-106">The following table lists the algorithm identifiers that are currently defined.</span></span> <span data-ttu-id="11013-107">Les auteurs des [*fournisseurs de services de chiffrement*](../secgloss/c-gly.md) (CSP) personnalisés peuvent définir de nouvelles valeurs.</span><span class="sxs-lookup"><span data-stu-id="11013-107">Authors of custom [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs) can define new values.</span></span> <span data-ttu-id="11013-108">En outre, les **ALG_ID** utilisés par des fournisseurs de services de chiffrement personnalisés pour les spécifications de clé **AT_KEYEXCHANGE** et **AT_SIGNATURE** dépendent du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="11013-108">Also, the **ALG_ID** used by custom CSPs for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are provider dependent.</span></span> <span data-ttu-id="11013-109">Les mappages actuels suivent le tableau.</span><span class="sxs-lookup"><span data-stu-id="11013-109">Current mappings follow the table.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11013-110">Identificateur</span><span class="sxs-lookup"><span data-stu-id="11013-110">Identifier</span></span></th>
<th><span data-ttu-id="11013-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="11013-111">Value</span></span></th>
<th><span data-ttu-id="11013-112">Description</span><span class="sxs-lookup"><span data-stu-id="11013-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11013-113">CALG_3DES</span><span class="sxs-lookup"><span data-stu-id="11013-113">CALG_3DES</span></span></td>
<td><span data-ttu-id="11013-114">0x00006603</span><span class="sxs-lookup"><span data-stu-id="11013-114">0x00006603</span></span></td>
<td><span data-ttu-id="11013-115">Algorithme de chiffrement <a href="/windows/desktop/SecGloss/t-gly"><em>triple des</em></a> .</span><span class="sxs-lookup"><span data-stu-id="11013-115"><a href="/windows/desktop/SecGloss/t-gly"><em>Triple DES</em></a> encryption algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-116">CALG_3DES_112</span><span class="sxs-lookup"><span data-stu-id="11013-116">CALG_3DES_112</span></span></td>
<td><span data-ttu-id="11013-117">0x00006609</span><span class="sxs-lookup"><span data-stu-id="11013-117">0x00006609</span></span></td>
<td><span data-ttu-id="11013-118">Chiffrement <a href="/windows/desktop/SecGloss/t-gly"><em>triple des</em></a> à deux clés avec une longueur de clé effective égale à 112 bits.</span><span class="sxs-lookup"><span data-stu-id="11013-118">Two-key <a href="/windows/desktop/SecGloss/t-gly"><em>triple DES</em></a> encryption with effective key length equal to 112 bits.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-119">CALG_AES</span><span class="sxs-lookup"><span data-stu-id="11013-119">CALG_AES</span></span></td>
<td><span data-ttu-id="11013-120">0x00006611</span><span class="sxs-lookup"><span data-stu-id="11013-120">0x00006611</span></span></td>
<td><span data-ttu-id="11013-121">Advanced Encryption Standard (AES).</span><span class="sxs-lookup"><span data-stu-id="11013-121">Advanced Encryption Standard (AES).</span></span> <span data-ttu-id="11013-122">Cet algorithme est pris en charge par le <a href="microsoft-aes-cryptographic-provider.md">fournisseur de services de chiffrement AES Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-122">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-123">CALG_AES_128</span><span class="sxs-lookup"><span data-stu-id="11013-123">CALG_AES_128</span></span></td>
<td><span data-ttu-id="11013-124">0x0000660e</span><span class="sxs-lookup"><span data-stu-id="11013-124">0x0000660e</span></span></td>
<td><span data-ttu-id="11013-125">AES 128 bits.</span><span class="sxs-lookup"><span data-stu-id="11013-125">128 bit AES.</span></span> <span data-ttu-id="11013-126">Cet algorithme est pris en charge par le <a href="microsoft-aes-cryptographic-provider.md">fournisseur de services de chiffrement AES Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-126">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-127">CALG_AES_192</span><span class="sxs-lookup"><span data-stu-id="11013-127">CALG_AES_192</span></span></td>
<td><span data-ttu-id="11013-128">0x0000660f</span><span class="sxs-lookup"><span data-stu-id="11013-128">0x0000660f</span></span></td>
<td><span data-ttu-id="11013-129">AES 192 bits.</span><span class="sxs-lookup"><span data-stu-id="11013-129">192 bit AES.</span></span> <span data-ttu-id="11013-130">Cet algorithme est pris en charge par le <a href="microsoft-aes-cryptographic-provider.md">fournisseur de services de chiffrement AES Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-130">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-131">CALG_AES_256</span><span class="sxs-lookup"><span data-stu-id="11013-131">CALG_AES_256</span></span></td>
<td><span data-ttu-id="11013-132">0x00006610</span><span class="sxs-lookup"><span data-stu-id="11013-132">0x00006610</span></span></td>
<td><span data-ttu-id="11013-133">AES 256 bits.</span><span class="sxs-lookup"><span data-stu-id="11013-133">256 bit AES.</span></span> <span data-ttu-id="11013-134">Cet algorithme est pris en charge par le <a href="microsoft-aes-cryptographic-provider.md">fournisseur de services de chiffrement AES Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-134">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-135">CALG_AGREEDKEY_ANY</span><span class="sxs-lookup"><span data-stu-id="11013-135">CALG_AGREEDKEY_ANY</span></span></td>
<td><span data-ttu-id="11013-136">0x0000aa03</span><span class="sxs-lookup"><span data-stu-id="11013-136">0x0000aa03</span></span></td>
<td><span data-ttu-id="11013-137">Identificateur d’algorithme temporaire pour les handles de Diffie-Hellman : clés convenues.</span><span class="sxs-lookup"><span data-stu-id="11013-137">Temporary algorithm identifier for handles of Diffie-Hellman–agreed keys.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-138">CALG_CYLINK_MEK</span><span class="sxs-lookup"><span data-stu-id="11013-138">CALG_CYLINK_MEK</span></span></td>
<td><span data-ttu-id="11013-139">0x0000660c</span><span class="sxs-lookup"><span data-stu-id="11013-139">0x0000660c</span></span></td>
<td><span data-ttu-id="11013-140">Algorithme permettant de créer une clé de 40 bits avec DES bits de parité et des bits de clé mis à zéro pour faire de la longueur de clé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="11013-140">An algorithm to create a 40-bit DES key that has parity bits and zeroed key bits to make its key length 64 bits.</span></span> <span data-ttu-id="11013-141">Cet algorithme est pris en charge par le <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-141">This algorithm is supported by the <a href=""></a><a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-142">CALG_DES</span><span class="sxs-lookup"><span data-stu-id="11013-142">CALG_DES</span></span></td>
<td><span data-ttu-id="11013-143">0x00006601</span><span class="sxs-lookup"><span data-stu-id="11013-143">0x00006601</span></span></td>
<td><span data-ttu-id="11013-144">Algorithme de chiffrement DES.</span><span class="sxs-lookup"><span data-stu-id="11013-144">DES encryption algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-145">CALG_DESX</span><span class="sxs-lookup"><span data-stu-id="11013-145">CALG_DESX</span></span></td>
<td><span data-ttu-id="11013-146">0x00006604</span><span class="sxs-lookup"><span data-stu-id="11013-146">0x00006604</span></span></td>
<td><span data-ttu-id="11013-147">Algorithme de chiffrement DESX.</span><span class="sxs-lookup"><span data-stu-id="11013-147">DESX encryption algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-148">CALG_DH_EPHEM</span><span class="sxs-lookup"><span data-stu-id="11013-148">CALG_DH_EPHEM</span></span></td>
<td><span data-ttu-id="11013-149">0x0000aa02</span><span class="sxs-lookup"><span data-stu-id="11013-149">0x0000aa02</span></span></td>
<td><span data-ttu-id="11013-150">Diffie-Hellman algorithme d’échange de clés éphémères.</span><span class="sxs-lookup"><span data-stu-id="11013-150">Diffie-Hellman ephemeral key exchange algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-151">CALG_DH_SF</span><span class="sxs-lookup"><span data-stu-id="11013-151">CALG_DH_SF</span></span></td>
<td><span data-ttu-id="11013-152">0x0000aa01</span><span class="sxs-lookup"><span data-stu-id="11013-152">0x0000aa01</span></span></td>
<td><span data-ttu-id="11013-153">Diffie-Hellman l’algorithme d’échange de clés de stockage et de transfert.</span><span class="sxs-lookup"><span data-stu-id="11013-153">Diffie-Hellman store and forward key exchange algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-154">CALG_DSS_SIGN</span><span class="sxs-lookup"><span data-stu-id="11013-154">CALG_DSS_SIGN</span></span></td>
<td><span data-ttu-id="11013-155">0x00002200</span><span class="sxs-lookup"><span data-stu-id="11013-155">0x00002200</span></span></td>
<td><span data-ttu-id="11013-156">Algorithme de signature de <a href="/windows/desktop/SecGloss/p-gly"><em>clé publique</em></a> DSA.</span><span class="sxs-lookup"><span data-stu-id="11013-156">DSA <a href="/windows/desktop/SecGloss/p-gly"><em>public key</em></a> signature algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-157">CALG_ECDH</span><span class="sxs-lookup"><span data-stu-id="11013-157">CALG_ECDH</span></span></td>
<td><span data-ttu-id="11013-158">0x0000aa05</span><span class="sxs-lookup"><span data-stu-id="11013-158">0x0000aa05</span></span></td>
<td><span data-ttu-id="11013-159">Algorithme d’échange de clés Diffie-Hellman à courbe elliptique.</span><span class="sxs-lookup"><span data-stu-id="11013-159">Elliptic curve Diffie-Hellman key exchange algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="11013-160">Cet algorithme est pris en charge uniquement par le biais de l' <a href="/windows/desktop/SecCNG/cng-portal">API de chiffrement : Next Generation</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-160">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="11013-161"><strong>Windows Server 2003 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="11013-161"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-162">CALG_ECDH_EPHEM</span><span class="sxs-lookup"><span data-stu-id="11013-162">CALG_ECDH_EPHEM</span></span></td>
<td><span data-ttu-id="11013-163">0x0000ae06</span><span class="sxs-lookup"><span data-stu-id="11013-163">0x0000ae06</span></span></td>
<td><span data-ttu-id="11013-164">Algorithme d’échange de clés Diffie-Hellman à courbe elliptique éphémère.</span><span class="sxs-lookup"><span data-stu-id="11013-164">Ephemeral elliptic curve Diffie-Hellman key exchange algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="11013-165">Cet algorithme est pris en charge uniquement par le biais de l' <a href="/windows/desktop/SecCNG/cng-portal">API de chiffrement : Next Generation</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-165">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="11013-166"><strong>Windows Server 2003 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="11013-166"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-167">CALG_ECDSA</span><span class="sxs-lookup"><span data-stu-id="11013-167">CALG_ECDSA</span></span></td>
<td><span data-ttu-id="11013-168">0x00002203</span><span class="sxs-lookup"><span data-stu-id="11013-168">0x00002203</span></span></td>
<td><span data-ttu-id="11013-169">Algorithme de signature numérique à courbe elliptique.</span><span class="sxs-lookup"><span data-stu-id="11013-169">Elliptic curve digital signature algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="11013-170">Cet algorithme est pris en charge uniquement par le biais de l' <a href="/windows/desktop/SecCNG/cng-portal">API de chiffrement : Next Generation</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-170">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="11013-171"><strong>Windows Server 2003 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="11013-171"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-172">CALG_ECMQV</span><span class="sxs-lookup"><span data-stu-id="11013-172">CALG_ECMQV</span></span></td>
<td><span data-ttu-id="11013-173">0x0000a001</span><span class="sxs-lookup"><span data-stu-id="11013-173">0x0000a001</span></span></td>
<td><span data-ttu-id="11013-174">Algorithme d’échange de clés elliptique Curve Menezes, qu et Vanstone (MQV).</span><span class="sxs-lookup"><span data-stu-id="11013-174">Elliptic curve Menezes, Qu, and Vanstone (MQV) key exchange algorithm.</span></span> <span data-ttu-id="11013-175">Cet algorithme n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="11013-175">This algorithm is not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-176">CALG_HASH_REPLACE_OWF</span><span class="sxs-lookup"><span data-stu-id="11013-176">CALG_HASH_REPLACE_OWF</span></span></td>
<td><span data-ttu-id="11013-177">0x0000800b</span><span class="sxs-lookup"><span data-stu-id="11013-177">0x0000800b</span></span></td>
<td><span data-ttu-id="11013-178">Algorithme de hachage de fonction unidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="11013-178">One way function hashing algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-179">CALG_HUGHES_MD5</span><span class="sxs-lookup"><span data-stu-id="11013-179">CALG_HUGHES_MD5</span></span></td>
<td><span data-ttu-id="11013-180">0x0000a003</span><span class="sxs-lookup"><span data-stu-id="11013-180">0x0000a003</span></span></td>
<td><span data-ttu-id="11013-181">Algorithme de hachage MD5 Hughes.</span><span class="sxs-lookup"><span data-stu-id="11013-181">Hughes MD5 hashing algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-182">CALG_HMAC</span><span class="sxs-lookup"><span data-stu-id="11013-182">CALG_HMAC</span></span></td>
<td><span data-ttu-id="11013-183">0x00008009</span><span class="sxs-lookup"><span data-stu-id="11013-183">0x00008009</span></span></td>
<td><span data-ttu-id="11013-184">Algorithme de hachage à clé HMAC.</span><span class="sxs-lookup"><span data-stu-id="11013-184">HMAC keyed hash algorithm.</span></span> <span data-ttu-id="11013-185">Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-185">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-186">CALG_KEA_KEYX</span><span class="sxs-lookup"><span data-stu-id="11013-186">CALG_KEA_KEYX</span></span></td>
<td><span data-ttu-id="11013-187">0x0000aa04</span><span class="sxs-lookup"><span data-stu-id="11013-187">0x0000aa04</span></span></td>
<td><span data-ttu-id="11013-188">Algorithme d’échange de clés KEA (FORTEZZA).</span><span class="sxs-lookup"><span data-stu-id="11013-188">KEA key exchange algorithm (FORTEZZA).</span></span> <span data-ttu-id="11013-189">Cet algorithme n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="11013-189">This algorithm is not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-190">CALG_MAC</span><span class="sxs-lookup"><span data-stu-id="11013-190">CALG_MAC</span></span></td>
<td><span data-ttu-id="11013-191">0x00008005</span><span class="sxs-lookup"><span data-stu-id="11013-191">0x00008005</span></span></td>
<td><span data-ttu-id="11013-192">Algorithme de hachage à clé <a href="/windows/desktop/SecGloss/m-gly"><em>Mac</em></a> .</span><span class="sxs-lookup"><span data-stu-id="11013-192"><a href="/windows/desktop/SecGloss/m-gly"><em>MAC</em></a> keyed hash algorithm.</span></span> <span data-ttu-id="11013-193">Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-193">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-194">CALG_MD2</span><span class="sxs-lookup"><span data-stu-id="11013-194">CALG_MD2</span></span></td>
<td><span data-ttu-id="11013-195">0x00008001</span><span class="sxs-lookup"><span data-stu-id="11013-195">0x00008001</span></span></td>
<td><span data-ttu-id="11013-196">Algorithme de hachage MD2.</span><span class="sxs-lookup"><span data-stu-id="11013-196">MD2 hashing algorithm.</span></span> <span data-ttu-id="11013-197">Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-197">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-198">CALG_MD4</span><span class="sxs-lookup"><span data-stu-id="11013-198">CALG_MD4</span></span></td>
<td><span data-ttu-id="11013-199">0x00008002</span><span class="sxs-lookup"><span data-stu-id="11013-199">0x00008002</span></span></td>
<td><span data-ttu-id="11013-200">Algorithme de hachage MD4.</span><span class="sxs-lookup"><span data-stu-id="11013-200">MD4 hashing algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-201">CALG_MD5</span><span class="sxs-lookup"><span data-stu-id="11013-201">CALG_MD5</span></span></td>
<td><span data-ttu-id="11013-202">0x00008003</span><span class="sxs-lookup"><span data-stu-id="11013-202">0x00008003</span></span></td>
<td><span data-ttu-id="11013-203">Algorithme de hachage MD5.</span><span class="sxs-lookup"><span data-stu-id="11013-203">MD5 hashing algorithm.</span></span> <span data-ttu-id="11013-204">Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-204">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-205">CALG_NO_SIGN</span><span class="sxs-lookup"><span data-stu-id="11013-205">CALG_NO_SIGN</span></span></td>
<td><span data-ttu-id="11013-206">0x00002000</span><span class="sxs-lookup"><span data-stu-id="11013-206">0x00002000</span></span></td>
<td><span data-ttu-id="11013-207">Pas d’algorithme de signature.</span><span class="sxs-lookup"><span data-stu-id="11013-207">No signature algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-208">CALG_OID_INFO_CNG_ONLY</span><span class="sxs-lookup"><span data-stu-id="11013-208">CALG_OID_INFO_CNG_ONLY</span></span></td>
<td><span data-ttu-id="11013-209">égale</span><span class="sxs-lookup"><span data-stu-id="11013-209">0xffffffff</span></span></td>
<td><span data-ttu-id="11013-210">L’algorithme est uniquement implémenté dans CNG.</span><span class="sxs-lookup"><span data-stu-id="11013-210">The algorithm is only implemented in CNG.</span></span> <span data-ttu-id="11013-211">La macro, IS_SPECIAL_OID_INFO_ALGID, peut être utilisée pour déterminer si un algorithme de chiffrement est pris en charge uniquement à l’aide des fonctions CNG.</span><span class="sxs-lookup"><span data-stu-id="11013-211">The macro, IS_SPECIAL_OID_INFO_ALGID, can be used to determine whether a cryptography algorithm is only supported by using the CNG functions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-212">CALG_OID_INFO_PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11013-212">CALG_OID_INFO_PARAMETERS</span></span></td>
<td><span data-ttu-id="11013-213">0xfffffffe</span><span class="sxs-lookup"><span data-stu-id="11013-213">0xfffffffe</span></span></td>
<td><span data-ttu-id="11013-214">L’algorithme est défini dans les paramètres encodés.</span><span class="sxs-lookup"><span data-stu-id="11013-214">The algorithm is defined in the encoded parameters.</span></span> <span data-ttu-id="11013-215">L’algorithme est pris en charge uniquement à l’aide de CNG.</span><span class="sxs-lookup"><span data-stu-id="11013-215">The algorithm is only supported by using CNG.</span></span> <span data-ttu-id="11013-216">La macro, IS_SPECIAL_OID_INFO_ALGID, peut être utilisée pour déterminer si un algorithme de chiffrement est pris en charge uniquement à l’aide des fonctions CNG.</span><span class="sxs-lookup"><span data-stu-id="11013-216">The macro, IS_SPECIAL_OID_INFO_ALGID, can be used to determine whether a cryptography algorithm is only supported by using the CNG functions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-217">CALG_PCT1_MASTER</span><span class="sxs-lookup"><span data-stu-id="11013-217">CALG_PCT1_MASTER</span></span></td>
<td><span data-ttu-id="11013-218">0x00004c04</span><span class="sxs-lookup"><span data-stu-id="11013-218">0x00004c04</span></span></td>
<td><span data-ttu-id="11013-219">Utilisé par le système d’exploitation Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="11013-219">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="11013-220">Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="11013-220">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-221">CALG_RC2</span><span class="sxs-lookup"><span data-stu-id="11013-221">CALG_RC2</span></span></td>
<td><span data-ttu-id="11013-222">0x00006602</span><span class="sxs-lookup"><span data-stu-id="11013-222">0x00006602</span></span></td>
<td><span data-ttu-id="11013-223">Algorithme de chiffrement par bloc RC2.</span><span class="sxs-lookup"><span data-stu-id="11013-223">RC2 block encryption algorithm.</span></span> <span data-ttu-id="11013-224">Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-224">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-225">CALG_RC4</span><span class="sxs-lookup"><span data-stu-id="11013-225">CALG_RC4</span></span></td>
<td><span data-ttu-id="11013-226">0x00006801</span><span class="sxs-lookup"><span data-stu-id="11013-226">0x00006801</span></span></td>
<td><span data-ttu-id="11013-227">Algorithme de chiffrement de flux RC4.</span><span class="sxs-lookup"><span data-stu-id="11013-227">RC4 stream encryption algorithm.</span></span> <span data-ttu-id="11013-228">Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-228">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-229">CALG_RC5</span><span class="sxs-lookup"><span data-stu-id="11013-229">CALG_RC5</span></span></td>
<td><span data-ttu-id="11013-230">0x0000660d</span><span class="sxs-lookup"><span data-stu-id="11013-230">0x0000660d</span></span></td>
<td><span data-ttu-id="11013-231">Algorithme de chiffrement par bloc RC5.</span><span class="sxs-lookup"><span data-stu-id="11013-231">RC5 block encryption algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-232">CALG_RSA_KEYX</span><span class="sxs-lookup"><span data-stu-id="11013-232">CALG_RSA_KEYX</span></span></td>
<td><span data-ttu-id="11013-233">0x0000a400</span><span class="sxs-lookup"><span data-stu-id="11013-233">0x0000a400</span></span></td>
<td><span data-ttu-id="11013-234">Algorithme d’échange de clés publiques RSA.</span><span class="sxs-lookup"><span data-stu-id="11013-234">RSA public key exchange algorithm.</span></span> <span data-ttu-id="11013-235">Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-235">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-236">CALG_RSA_SIGN</span><span class="sxs-lookup"><span data-stu-id="11013-236">CALG_RSA_SIGN</span></span></td>
<td><span data-ttu-id="11013-237">0x00002400</span><span class="sxs-lookup"><span data-stu-id="11013-237">0x00002400</span></span></td>
<td><span data-ttu-id="11013-238">Algorithme de signature de clé publique RSA.</span><span class="sxs-lookup"><span data-stu-id="11013-238">RSA public key signature algorithm.</span></span> <span data-ttu-id="11013-239">Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-239">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-240">CALG_SCHANNEL_ENC_KEY</span><span class="sxs-lookup"><span data-stu-id="11013-240">CALG_SCHANNEL_ENC_KEY</span></span></td>
<td><span data-ttu-id="11013-241">0x00004c07</span><span class="sxs-lookup"><span data-stu-id="11013-241">0x00004c07</span></span></td>
<td><span data-ttu-id="11013-242">Utilisé par le système d’exploitation Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="11013-242">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="11013-243">Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="11013-243">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-244">CALG_SCHANNEL_MAC_KEY</span><span class="sxs-lookup"><span data-stu-id="11013-244">CALG_SCHANNEL_MAC_KEY</span></span></td>
<td><span data-ttu-id="11013-245">0x00004c03</span><span class="sxs-lookup"><span data-stu-id="11013-245">0x00004c03</span></span></td>
<td><span data-ttu-id="11013-246">Utilisé par le système d’exploitation Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="11013-246">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="11013-247">Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="11013-247">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-248">CALG_SCHANNEL_MASTER_HASH</span><span class="sxs-lookup"><span data-stu-id="11013-248">CALG_SCHANNEL_MASTER_HASH</span></span></td>
<td><span data-ttu-id="11013-249">0x00004c02</span><span class="sxs-lookup"><span data-stu-id="11013-249">0x00004c02</span></span></td>
<td><span data-ttu-id="11013-250">Utilisé par le système d’exploitation Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="11013-250">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="11013-251">Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="11013-251">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-252">CALG_SEAL</span><span class="sxs-lookup"><span data-stu-id="11013-252">CALG_SEAL</span></span></td>
<td><span data-ttu-id="11013-253">0x00006802</span><span class="sxs-lookup"><span data-stu-id="11013-253">0x00006802</span></span></td>
<td><span data-ttu-id="11013-254">SCELLe l’algorithme de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="11013-254">SEAL encryption algorithm.</span></span> <span data-ttu-id="11013-255">Cet algorithme n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="11013-255">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-256">CALG_SHA</span><span class="sxs-lookup"><span data-stu-id="11013-256">CALG_SHA</span></span></td>
<td><span data-ttu-id="11013-257">0x00008004</span><span class="sxs-lookup"><span data-stu-id="11013-257">0x00008004</span></span></td>
<td><span data-ttu-id="11013-258">Algorithme de hachage SHA.</span><span class="sxs-lookup"><span data-stu-id="11013-258">SHA hashing algorithm.</span></span> <span data-ttu-id="11013-259">Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-259">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-260">CALG_SHA1</span><span class="sxs-lookup"><span data-stu-id="11013-260">CALG_SHA1</span></span></td>
<td><span data-ttu-id="11013-261">0x00008004</span><span class="sxs-lookup"><span data-stu-id="11013-261">0x00008004</span></span></td>
<td><span data-ttu-id="11013-262">Identique à <strong>CALG_SHA</strong>.</span><span class="sxs-lookup"><span data-stu-id="11013-262">Same as <strong>CALG_SHA</strong>.</span></span> <span data-ttu-id="11013-263">Cet algorithme est pris en charge par le <a href="microsoft-base-cryptographic-provider.md">fournisseur de services de chiffrement de base Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="11013-263">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-264">CALG_SHA_256</span><span class="sxs-lookup"><span data-stu-id="11013-264">CALG_SHA_256</span></span></td>
<td><span data-ttu-id="11013-265">0x0000800c</span><span class="sxs-lookup"><span data-stu-id="11013-265">0x0000800c</span></span></td>
<td><span data-ttu-id="11013-266">algorithme de hachage SHA de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="11013-266">256 bit SHA hashing algorithm.</span></span> <span data-ttu-id="11013-267">Cet algorithme est pris en charge par Microsoft Enhanced RSA et le fournisseur de services de chiffrement AES. <strong>Windows XP avec SP3 :</strong> Cet algorithme est pris en charge par le fournisseur de services de chiffrement RSA et AES Microsoft amélioré (prototype).</span><span class="sxs-lookup"><span data-stu-id="11013-267">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider..<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="11013-268"><strong>Windows XP avec SP2, Windows XP avec SP1 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="11013-268"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-269">CALG_SHA_384</span><span class="sxs-lookup"><span data-stu-id="11013-269">CALG_SHA_384</span></span></td>
<td><span data-ttu-id="11013-270">0x0000800d</span><span class="sxs-lookup"><span data-stu-id="11013-270">0x0000800d</span></span></td>
<td><span data-ttu-id="11013-271">algorithme de hachage SHA de 384 bits.</span><span class="sxs-lookup"><span data-stu-id="11013-271">384 bit SHA hashing algorithm.</span></span> <span data-ttu-id="11013-272">Cet algorithme est pris en charge par Microsoft Enhanced RSA et le fournisseur de services de chiffrement AES. <strong>Windows XP avec SP3 :</strong> Cet algorithme est pris en charge par le fournisseur de services de chiffrement RSA et AES Microsoft amélioré (prototype).</span><span class="sxs-lookup"><span data-stu-id="11013-272">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider.<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="11013-273"><strong>Windows XP avec SP2, Windows XP avec SP1 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="11013-273"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-274">CALG_SHA_512</span><span class="sxs-lookup"><span data-stu-id="11013-274">CALG_SHA_512</span></span></td>
<td><span data-ttu-id="11013-275">0x0000800e</span><span class="sxs-lookup"><span data-stu-id="11013-275">0x0000800e</span></span></td>
<td><span data-ttu-id="11013-276">algorithme de hachage SHA de 512 bits.</span><span class="sxs-lookup"><span data-stu-id="11013-276">512 bit SHA hashing algorithm.</span></span> <span data-ttu-id="11013-277">Cet algorithme est pris en charge par Microsoft Enhanced RSA et le fournisseur de services de chiffrement AES. <strong>Windows XP avec SP3 :</strong> Cet algorithme est pris en charge par le fournisseur de services de chiffrement RSA et AES Microsoft amélioré (prototype).</span><span class="sxs-lookup"><span data-stu-id="11013-277">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider.<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="11013-278"><strong>Windows XP avec SP2, Windows XP avec SP1 et Windows XP :</strong> Cet algorithme n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="11013-278"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-279">CALG_SKIPJACK</span><span class="sxs-lookup"><span data-stu-id="11013-279">CALG_SKIPJACK</span></span></td>
<td><span data-ttu-id="11013-280">0x0000660a</span><span class="sxs-lookup"><span data-stu-id="11013-280">0x0000660a</span></span></td>
<td><span data-ttu-id="11013-281">Algorithme de chiffrement par bloc Skipjack (FORTEZZA).</span><span class="sxs-lookup"><span data-stu-id="11013-281">Skipjack block encryption algorithm (FORTEZZA).</span></span> <span data-ttu-id="11013-282">Cet algorithme n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="11013-282">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-283">CALG_SSL2_MASTER</span><span class="sxs-lookup"><span data-stu-id="11013-283">CALG_SSL2_MASTER</span></span></td>
<td><span data-ttu-id="11013-284">0x00004c05</span><span class="sxs-lookup"><span data-stu-id="11013-284">0x00004c05</span></span></td>
<td><span data-ttu-id="11013-285">Utilisé par le système d’exploitation Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="11013-285">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="11013-286">Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="11013-286">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-287">CALG_SSL3_MASTER</span><span class="sxs-lookup"><span data-stu-id="11013-287">CALG_SSL3_MASTER</span></span></td>
<td><span data-ttu-id="11013-288">0x00004c01</span><span class="sxs-lookup"><span data-stu-id="11013-288">0x00004c01</span></span></td>
<td><span data-ttu-id="11013-289">Utilisé par le système d’exploitation Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="11013-289">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="11013-290">Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="11013-290">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-291">CALG_SSL3_SHAMD5</span><span class="sxs-lookup"><span data-stu-id="11013-291">CALG_SSL3_SHAMD5</span></span></td>
<td><span data-ttu-id="11013-292">0x00008008</span><span class="sxs-lookup"><span data-stu-id="11013-292">0x00008008</span></span></td>
<td><span data-ttu-id="11013-293">Utilisé par le système d’exploitation Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="11013-293">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="11013-294">Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="11013-294">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-295">CALG_TEK</span><span class="sxs-lookup"><span data-stu-id="11013-295">CALG_TEK</span></span></td>
<td><span data-ttu-id="11013-296">0x0000660b</span><span class="sxs-lookup"><span data-stu-id="11013-296">0x0000660b</span></span></td>
<td><span data-ttu-id="11013-297">TEK (FORTEZZA).</span><span class="sxs-lookup"><span data-stu-id="11013-297">TEK (FORTEZZA).</span></span> <span data-ttu-id="11013-298">Cet algorithme n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="11013-298">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11013-299">CALG_TLS1_MASTER</span><span class="sxs-lookup"><span data-stu-id="11013-299">CALG_TLS1_MASTER</span></span></td>
<td><span data-ttu-id="11013-300">0x00004c06</span><span class="sxs-lookup"><span data-stu-id="11013-300">0x00004c06</span></span></td>
<td><span data-ttu-id="11013-301">Utilisé par le système d’exploitation Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="11013-301">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="11013-302">Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="11013-302">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11013-303">CALG_TLS1PRF</span><span class="sxs-lookup"><span data-stu-id="11013-303">CALG_TLS1PRF</span></span></td>
<td><span data-ttu-id="11013-304">0x0000800a</span><span class="sxs-lookup"><span data-stu-id="11013-304">0x0000800a</span></span></td>
<td><span data-ttu-id="11013-305">Utilisé par le système d’exploitation Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="11013-305">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="11013-306">Cette <strong>ALG_ID</strong> ne doit pas être utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="11013-306">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="11013-307">Pour le [fournisseur de services de chiffrement de base Microsoft](microsoft-base-cryptographic-provider.md), le fournisseur de services de chiffrement [renforcé](microsoft-strong-cryptographic-provider.md)Microsoft et le [fournisseur de services de chiffrement amélioré Microsoft](microsoft-enhanced-cryptographic-provider.md), les **ALG_IDs** utilisés pour les spécifications de clé **AT_KEYEXCHANGE** et **AT_SIGNATURE** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="11013-307">For the [Microsoft Base Cryptographic Provider](microsoft-base-cryptographic-provider.md), the [Microsoft Strong Cryptographic Provider](microsoft-strong-cryptographic-provider.md), and the [Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md), the **ALG_IDs** used for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are as follows:</span></span>

-   <span data-ttu-id="11013-308">**CALG_RSA_KEYX** est utilisé pour les **AT_KEYEXCHANGE**.</span><span class="sxs-lookup"><span data-stu-id="11013-308">**CALG_RSA_KEYX** is used for **AT_KEYEXCHANGE**.</span></span>
-   <span data-ttu-id="11013-309">**CALG_RSA_SIGN** est utilisé pour les **AT_SIGNATURE**.</span><span class="sxs-lookup"><span data-stu-id="11013-309">**CALG_RSA_SIGN** is used for **AT_SIGNATURE**.</span></span>

<span data-ttu-id="11013-310">Pour les [fournisseurs de services de chiffrement DSS et Diffie-Hellman de base Microsoft](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), les **ALG_IDs** utilisés pour les spécifications de clé **AT_KEYEXCHANGE** et **AT_SIGNATURE** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="11013-310">For the [Microsoft Base DSS and Diffie-Hellman Cryptographic Provider](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), the **ALG_IDs** used for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are as follows:</span></span>

-   <span data-ttu-id="11013-311">**CALG_DH_SF** est utilisé pour les **AT_KEYEXCHANGE**.</span><span class="sxs-lookup"><span data-stu-id="11013-311">**CALG_DH_SF** is used for **AT_KEYEXCHANGE**.</span></span>
-   <span data-ttu-id="11013-312">**CALG_DSS_SIGN** est utilisé pour les **AT_SIGNATURE**.</span><span class="sxs-lookup"><span data-stu-id="11013-312">**CALG_DSS_SIGN** is used for **AT_SIGNATURE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="11013-313">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11013-313">Requirements</span></span>



| <span data-ttu-id="11013-314">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11013-314">Requirement</span></span> | <span data-ttu-id="11013-315">Valeur</span><span class="sxs-lookup"><span data-stu-id="11013-315">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11013-316">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11013-316">Minimum supported client</span></span><br/> | <span data-ttu-id="11013-317">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11013-317">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="11013-318">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11013-318">Minimum supported server</span></span><br/> | <span data-ttu-id="11013-319">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11013-319">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11013-320">En-tête</span><span class="sxs-lookup"><span data-stu-id="11013-320">Header</span></span><br/>                   | <dl> <span data-ttu-id="11013-321"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="11013-321"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11013-322">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11013-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11013-323">Fonctions de chiffrement</span><span class="sxs-lookup"><span data-stu-id="11013-323">Cryptography Functions</span></span>](cryptography-functions.md)
</dt> <dt>

[<span data-ttu-id="11013-324">**CRYPT_ALGORITHM_IDENTIFIER**</span><span class="sxs-lookup"><span data-stu-id="11013-324">**CRYPT_ALGORITHM_IDENTIFIER**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[<span data-ttu-id="11013-325">**CryptFindOIDInfo**</span><span class="sxs-lookup"><span data-stu-id="11013-325">**CryptFindOIDInfo**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
