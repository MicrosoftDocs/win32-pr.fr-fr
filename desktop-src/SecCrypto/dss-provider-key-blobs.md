---
description: Utilisé avec le fournisseur DSS (Digital Signature standard) pour exporter les clés et importer les clés dans, le fournisseur de services de chiffrement (CSP).
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: Objets BLOB de clé du fournisseur DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27a73e35cccd6fad672f4c94d589d754f970c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951086"
---
# <a name="dss-provider-key-blobs"></a><span data-ttu-id="23918-103">Objets BLOB de clé du fournisseur DSS</span><span class="sxs-lookup"><span data-stu-id="23918-103">DSS Provider Key BLOBs</span></span>

<span data-ttu-id="23918-104">Les [*objets BLOB*](../secgloss/b-gly.md) sont utilisés avec le fournisseur DSS ( [*Digital Signature standard*](../secgloss/d-gly.md) ) pour exporter les clés et importer les clés dans, le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="23918-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Digital Signature Standard*](../secgloss/d-gly.md) (DSS) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="23918-105">Objets BLOB de clé publique</span><span class="sxs-lookup"><span data-stu-id="23918-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="23918-106">Objets BLOB de clé privée</span><span class="sxs-lookup"><span data-stu-id="23918-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="23918-107">Objets BLOB de clé publique</span><span class="sxs-lookup"><span data-stu-id="23918-107">Public Key BLOBs</span></span>

<span data-ttu-id="23918-108">Une [*clé publique*](../secgloss/p-gly.md) DSS est exportée et importée en tant qu’objet BLOB, une séquence d’octets structurée comme suit.</span><span class="sxs-lookup"><span data-stu-id="23918-108">A DSS [*public key*](../secgloss/p-gly.md) is exported and imported as a BLOB, a sequence of bytes structured as follows.</span></span>

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

<span data-ttu-id="23918-109">Le tableau suivant décrit ces composants.</span><span class="sxs-lookup"><span data-stu-id="23918-109">The following table describes these components.</span></span> <span data-ttu-id="23918-110">Toutes les valeurs sont au format [*Little endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="23918-110">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="23918-111">Champ</span><span class="sxs-lookup"><span data-stu-id="23918-111">Field</span></span>          | <span data-ttu-id="23918-112">Description</span><span class="sxs-lookup"><span data-stu-id="23918-112">Description</span></span>                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23918-113">dsspubkey</span><span class="sxs-lookup"><span data-stu-id="23918-113">dsspubkey</span></span>      | <span data-ttu-id="23918-114">Structure [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="23918-114">A [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) structure.</span></span> <span data-ttu-id="23918-115">Le membre **magique** doit avoir la valeur 0x31535344.</span><span class="sxs-lookup"><span data-stu-id="23918-115">The **magic** member must have a value of 0x31535344.</span></span> <span data-ttu-id="23918-116">Ce nombre hexadécimal est l’encodage [*ASCII*](../secgloss/a-gly.md) de DSS1.</span><span class="sxs-lookup"><span data-stu-id="23918-116">This hexadecimal number is the [*ASCII*](../secgloss/a-gly.md) encoding of DSS1.</span></span> |
| <span data-ttu-id="23918-117">g</span><span class="sxs-lookup"><span data-stu-id="23918-117">g</span></span>              | <span data-ttu-id="23918-118">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="23918-118">A **BYTE** sequence.</span></span> <span data-ttu-id="23918-119">Générateur, g.</span><span class="sxs-lookup"><span data-stu-id="23918-119">The generator, g.</span></span> <span data-ttu-id="23918-120">Doit avoir la même longueur que p.</span><span class="sxs-lookup"><span data-stu-id="23918-120">Must be the same length as p.</span></span> <span data-ttu-id="23918-121">S’il n’est pas de la même longueur que p, il doit être rempli avec 0x00 octets.</span><span class="sxs-lookup"><span data-stu-id="23918-121">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                      |
| <span data-ttu-id="23918-122">p</span><span class="sxs-lookup"><span data-stu-id="23918-122">p</span></span>              | <span data-ttu-id="23918-123">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="23918-123">A **BYTE** sequence.</span></span> <span data-ttu-id="23918-124">Le modulo principal, p.</span><span class="sxs-lookup"><span data-stu-id="23918-124">The prime modulus, p.</span></span> <span data-ttu-id="23918-125">Le bit le plus significatif de l’octet le plus significatif doit être défini sur un.</span><span class="sxs-lookup"><span data-stu-id="23918-125">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                                 |
| <span data-ttu-id="23918-126">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="23918-126">publickeystruc</span></span> | <span data-ttu-id="23918-127">Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="23918-127">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                |
| <span data-ttu-id="23918-128">q</span><span class="sxs-lookup"><span data-stu-id="23918-128">q</span></span>              | <span data-ttu-id="23918-129">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="23918-129">A **BYTE** sequence.</span></span> <span data-ttu-id="23918-130">La longueur prime, q, 20 octets.</span><span class="sxs-lookup"><span data-stu-id="23918-130">The prime, q, 20 bytes in length.</span></span> <span data-ttu-id="23918-131">Le bit le plus significatif de l’octet le plus significatif doit être défini sur un.</span><span class="sxs-lookup"><span data-stu-id="23918-131">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                     |
| <span data-ttu-id="23918-132">seedstruct</span><span class="sxs-lookup"><span data-stu-id="23918-132">seedstruct</span></span>     | <span data-ttu-id="23918-133">Structure [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) .</span><span class="sxs-lookup"><span data-stu-id="23918-133">A [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) structure.</span></span> <span data-ttu-id="23918-134">Valeurs de départ et de compteur pour la vérification des premiers.</span><span class="sxs-lookup"><span data-stu-id="23918-134">Seed and counter values for verifying primes.</span></span>                                                                                                                                |
| <span data-ttu-id="23918-135">y</span><span class="sxs-lookup"><span data-stu-id="23918-135">y</span></span>              | <span data-ttu-id="23918-136">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="23918-136">A **BYTE** sequence.</span></span> <span data-ttu-id="23918-137">Clé publique, y.</span><span class="sxs-lookup"><span data-stu-id="23918-137">The public key, y.</span></span> <span data-ttu-id="23918-138">Doit avoir la même longueur que p.</span><span class="sxs-lookup"><span data-stu-id="23918-138">Must be same length as p.</span></span> <span data-ttu-id="23918-139">S’il n’est pas de la même longueur que p, il doit être rempli avec 0x00 octets.</span><span class="sxs-lookup"><span data-stu-id="23918-139">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                         |



 

> [!Note]  
> <span data-ttu-id="23918-140">Les [*objets BLOB de clé publique*](../secgloss/p-gly.md) ne sont pas chiffrés.</span><span class="sxs-lookup"><span data-stu-id="23918-140">[*Public key BLOBs*](../secgloss/p-gly.md) are not encrypted.</span></span> <span data-ttu-id="23918-141">Elles contiennent des clés publiques sous forme de [*texte en clair*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="23918-141">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="23918-142">Objets BLOB de clé privée</span><span class="sxs-lookup"><span data-stu-id="23918-142">Private Key BLOBs</span></span>

<span data-ttu-id="23918-143">Une [*clé privée*](../secgloss/p-gly.md) DSS est exportée et importée sous la forme d’une séquence d’octets structurée comme suit.</span><span class="sxs-lookup"><span data-stu-id="23918-143">A DSS [*private key*](../secgloss/p-gly.md) is exported and imported as a sequence of bytes structured as follows.</span></span>

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

<span data-ttu-id="23918-144">Le tableau suivant décrit chaque composant.</span><span class="sxs-lookup"><span data-stu-id="23918-144">The following table describes each component.</span></span> <span data-ttu-id="23918-145">Toutes les valeurs sont au format [*Little endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="23918-145">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="23918-146">Champ</span><span class="sxs-lookup"><span data-stu-id="23918-146">Field</span></span>          | <span data-ttu-id="23918-147">Description</span><span class="sxs-lookup"><span data-stu-id="23918-147">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23918-148">dsspubkey</span><span class="sxs-lookup"><span data-stu-id="23918-148">dsspubkey</span></span>      | <span data-ttu-id="23918-149">Structure [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="23918-149">A [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) structure.</span></span> <span data-ttu-id="23918-150">Le membre **magique** doit être défini sur 0x32535344.</span><span class="sxs-lookup"><span data-stu-id="23918-150">The **magic** member must be set to 0x32535344.</span></span> <span data-ttu-id="23918-151">Ce nombre hexadécimal est l’encodage [*ASCII*](../secgloss/a-gly.md) de DSS2.</span><span class="sxs-lookup"><span data-stu-id="23918-151">This hexadecimal number is the [*ASCII*](../secgloss/a-gly.md) encoding of DSS2.</span></span> |
| <span data-ttu-id="23918-152">g</span><span class="sxs-lookup"><span data-stu-id="23918-152">g</span></span>              | <span data-ttu-id="23918-153">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="23918-153">A **BYTE** sequence.</span></span> <span data-ttu-id="23918-154">Générateur, g.</span><span class="sxs-lookup"><span data-stu-id="23918-154">The generator, g.</span></span> <span data-ttu-id="23918-155">Doit avoir la même longueur que p.</span><span class="sxs-lookup"><span data-stu-id="23918-155">Must be the same length as p.</span></span> <span data-ttu-id="23918-156">S’il n’est pas de la même longueur que p, il doit être rempli avec 0x00 octets.</span><span class="sxs-lookup"><span data-stu-id="23918-156">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                |
| <span data-ttu-id="23918-157">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="23918-157">publickeystruc</span></span> | <span data-ttu-id="23918-158">Structure [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="23918-158">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                          |
| <span data-ttu-id="23918-159">p</span><span class="sxs-lookup"><span data-stu-id="23918-159">p</span></span>              | <span data-ttu-id="23918-160">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="23918-160">A **BYTE** sequence.</span></span> <span data-ttu-id="23918-161">Le modulo principal, p.</span><span class="sxs-lookup"><span data-stu-id="23918-161">The prime modulus, p.</span></span> <span data-ttu-id="23918-162">Le bit le plus significatif de l’octet le plus significatif doit être défini sur un.</span><span class="sxs-lookup"><span data-stu-id="23918-162">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                           |
| <span data-ttu-id="23918-163">q</span><span class="sxs-lookup"><span data-stu-id="23918-163">q</span></span>              | <span data-ttu-id="23918-164">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="23918-164">A **BYTE** sequence.</span></span> <span data-ttu-id="23918-165">Le premier, le q.</span><span class="sxs-lookup"><span data-stu-id="23918-165">The prime, q.</span></span> <span data-ttu-id="23918-166">q a une longueur de 20 octets.</span><span class="sxs-lookup"><span data-stu-id="23918-166">q is 20 bytes in length.</span></span> <span data-ttu-id="23918-167">Le bit le plus significatif de l’octet le plus significatif doit être défini sur un.</span><span class="sxs-lookup"><span data-stu-id="23918-167">The most significant bit of the most significant byte must be set to one.</span></span>                                                                          |
| <span data-ttu-id="23918-168">seedstruct</span><span class="sxs-lookup"><span data-stu-id="23918-168">seedstruct</span></span>     | <span data-ttu-id="23918-169">Structure [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) .</span><span class="sxs-lookup"><span data-stu-id="23918-169">A [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) structure.</span></span> <span data-ttu-id="23918-170">Valeurs de départ et de compteur pour la vérification des premiers.</span><span class="sxs-lookup"><span data-stu-id="23918-170">Seed and counter values for verifying primes.</span></span>                                                                                                                          |
| <span data-ttu-id="23918-171">x</span><span class="sxs-lookup"><span data-stu-id="23918-171">x</span></span>              | <span data-ttu-id="23918-172">Séquence d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="23918-172">A **BYTE** sequence.</span></span> <span data-ttu-id="23918-173">Exposant secret, x.</span><span class="sxs-lookup"><span data-stu-id="23918-173">The secret exponent, x.</span></span> <span data-ttu-id="23918-174">Doit toujours avoir une longueur de 20 octets.</span><span class="sxs-lookup"><span data-stu-id="23918-174">Must always be 20 bytes in length.</span></span> <span data-ttu-id="23918-175">Si x a une longueur inférieure à 20 octets, elle doit être remplie avec 0x00.</span><span class="sxs-lookup"><span data-stu-id="23918-175">If x is smaller than 20 bytes in length, then it must be padded with 0x00.</span></span>                                                     |



 

<span data-ttu-id="23918-176">Lors de l’appel de [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), le développeur peut choisir de chiffrer ou non la clé.</span><span class="sxs-lookup"><span data-stu-id="23918-176">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="23918-177">Le **PRIVATEKEYBLOB** est chiffré si le paramètre *hExpKey* contient un handle valide pour une clé de session.</span><span class="sxs-lookup"><span data-stu-id="23918-177">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="23918-178">Tout sauf la partie [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) de l’objet blob est chiffré.</span><span class="sxs-lookup"><span data-stu-id="23918-178">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="23918-179">Les paramètres d’algorithme de chiffrement et de clé de chiffrement ne sont pas stockés avec l’objet BLOB de clé privée.</span><span class="sxs-lookup"><span data-stu-id="23918-179">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="23918-180">L’application doit gérer et stocker ces informations.</span><span class="sxs-lookup"><span data-stu-id="23918-180">The application must manage and store this information.</span></span> <span data-ttu-id="23918-181">Si la valeur zéro est passée pour *hExpKey*, la clé privée est exportée sans chiffrement.</span><span class="sxs-lookup"><span data-stu-id="23918-181">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="23918-182">Il est dangereux d’exporter les clés privées sans chiffrement, car elles sont ensuite vulnérables à l’interception et à l’utilisation par des entités non autorisées.</span><span class="sxs-lookup"><span data-stu-id="23918-182">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

 

 
