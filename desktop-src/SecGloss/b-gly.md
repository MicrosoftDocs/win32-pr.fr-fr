---
description: Contient les définitions des termes de sécurité qui commencent par la lettre B.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2e570727-7da0-4e17-bf5d-6fe0e6aef65b
title: B (Glossaire de la sécurité)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40aedaebddb86ddf9f32a9a3d86cf4cf4a613642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520683"
---
# <a name="b-security-glossary"></a><span data-ttu-id="3582d-103">B (Glossaire de la sécurité)</span><span class="sxs-lookup"><span data-stu-id="3582d-103">B (Security Glossary)</span></span>

<span data-ttu-id="3582d-104">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="3582d-104">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="3582d-105"><span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**autorité de sauvegarde**</span><span class="sxs-lookup"><span data-stu-id="3582d-105"><span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**backup authority**</span></span>
</dt> <dd>

<span data-ttu-id="3582d-106">Application approuvée s’exécutant sur un ordinateur sécurisé qui fournit un stockage secondaire pour les clés de session de ses clients.</span><span class="sxs-lookup"><span data-stu-id="3582d-106">A trusted application running on a secure computer that provides secondary storage for the session keys of its clients.</span></span> <span data-ttu-id="3582d-107">L’autorité de sauvegarde stocke les clés de session en tant qu’objets BLOB de clé chiffrés avec la clé publique de l’autorité de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="3582d-107">The backup authority stores session keys as key BLOBs that are encrypted with the backup authority's public key.</span></span>

</dd> <dt>

<span data-ttu-id="3582d-108"><span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**type de contenu de base**</span><span class="sxs-lookup"><span data-stu-id="3582d-108"><span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**base content type**</span></span>
</dt> <dd>

<span data-ttu-id="3582d-109">Type de données contenu dans un message PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="3582d-109">A type of data contained in a PKCS \#7 message.</span></span> <span data-ttu-id="3582d-110">Les types de contenu de base contiennent uniquement des données, aucune amélioration de chiffrement telle que les hachages ou les signatures.</span><span class="sxs-lookup"><span data-stu-id="3582d-110">Base content types only contain data, no cryptographic enhancements such as hashes or signatures.</span></span> <span data-ttu-id="3582d-111">Actuellement, le seul type de contenu de base est le type de contenu de données.</span><span class="sxs-lookup"><span data-stu-id="3582d-111">Currently, the only base content type is the Data content type.</span></span>

</dd> <dt>

<span data-ttu-id="3582d-112"><span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**fonctions de chiffrement de base**</span><span class="sxs-lookup"><span data-stu-id="3582d-112"><span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**base cryptographic functions**</span></span>
</dt> <dd>

<span data-ttu-id="3582d-113">Niveau le plus bas des fonctions dans l’architecture CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="3582d-113">The lowest level of functions in the CryptoAPI architecture.</span></span> <span data-ttu-id="3582d-114">Ils sont utilisés par les applications et d’autres fonctions CryptoAPI de haut niveau pour fournir un accès aux algorithmes de chiffrement fournis par le fournisseur de solutions de chiffrement, à la génération de clés sécurisées et au stockage sécurisé des secrets.</span><span class="sxs-lookup"><span data-stu-id="3582d-114">They are used by applications and other high-level CryptoAPI functions to provide access to CSP-provided cryptographic algorithms, secure key generation, and secure storage of secrets.</span></span>

<span data-ttu-id="3582d-115">Voir aussi [*fournisseurs de services de chiffrement*](c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3582d-115">See also [*cryptographic service providers*](c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="3582d-116"><span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**Règles d’encodage de base**</span><span class="sxs-lookup"><span data-stu-id="3582d-116"><span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**Basic Encoding Rules**</span></span>
</dt> <dd>

<span data-ttu-id="3582d-117">BER Ensemble de règles utilisées pour encoder les données ASN. 1 définies en un flux de bits (zéros ou autres) pour le stockage ou la transmission externes.</span><span class="sxs-lookup"><span data-stu-id="3582d-117">(BER) The set of rules used to encode ASN.1 defined data into a stream of bits (zeros or ones) for external storage or transmission.</span></span> <span data-ttu-id="3582d-118">Un seul objet ASN. 1 peut avoir plusieurs encodages BER équivalents.</span><span class="sxs-lookup"><span data-stu-id="3582d-118">A single ASN.1 object may have several equivalent BER encodes.</span></span> <span data-ttu-id="3582d-119">BER est défini dans la recommandation CCITT X. 209.</span><span class="sxs-lookup"><span data-stu-id="3582d-119">BER is defined in CCITT Recommendation X.209.</span></span> <span data-ttu-id="3582d-120">Il s’agit de l’une des deux méthodes d’encodage actuellement utilisées par CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="3582d-120">This is one of the two encoding methods currently used by CryptoAPI.</span></span>

</dd> <dt>

<span data-ttu-id="3582d-121"><span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**BER**</span><span class="sxs-lookup"><span data-stu-id="3582d-121"><span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**BER**</span></span>
</dt> <dd>

<span data-ttu-id="3582d-122">Consultez *règles d’encodage de base*.</span><span class="sxs-lookup"><span data-stu-id="3582d-122">See *Basic Encoding Rules*.</span></span>

</dd> <dt>

<span data-ttu-id="3582d-123"><span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**Big endian**</span><span class="sxs-lookup"><span data-stu-id="3582d-123"><span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**big-endian**</span></span>
</dt> <dd>

<span data-ttu-id="3582d-124">Un format de mémoire ou de données dans lequel l’octet le plus significatif est stocké à l’adresse inférieure ou qui arrive en premier.</span><span class="sxs-lookup"><span data-stu-id="3582d-124">A memory or data format in which the most significant byte is stored at the lower address or arrives first.</span></span>

<span data-ttu-id="3582d-125">Voir aussi [*Little endian*](l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3582d-125">See also [*little-endian*](l-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="3582d-126"><span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**OBJET BLOB**</span><span class="sxs-lookup"><span data-stu-id="3582d-126"><span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="3582d-127">Séquence générique de bits qui contiennent une ou plusieurs structures d’en-tête de longueur fixe, ainsi que des données spécifiques au contexte.</span><span class="sxs-lookup"><span data-stu-id="3582d-127">A generic sequence of bits that contain one or more fixed-length header structures plus context specific data.</span></span>

<span data-ttu-id="3582d-128">Voir aussi [*objets BLOB de clé*](k-gly.md), [*objets BLOB de certificat*](c-gly.md), objets BLOB de [*nom de certificat*](c-gly.md)et [*objets BLOB d’attribut*](a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3582d-128">See also [*key BLOBs*](k-gly.md), [*certificate BLOBs*](c-gly.md), [*certificate name BLOBs*](c-gly.md), and [*attribute BLOBs*](a-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="3582d-129"><span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**chiffrement par bloc**</span><span class="sxs-lookup"><span data-stu-id="3582d-129"><span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**block cipher**</span></span>
</dt> <dd>

<span data-ttu-id="3582d-130">Algorithme de chiffrement qui chiffre les données en unités discrètes (appelées blocs), plutôt qu’en tant que flux continu de bits.</span><span class="sxs-lookup"><span data-stu-id="3582d-130">A cipher algorithm that encrypts data in discrete units (called blocks), rather than as a continuous stream of bits.</span></span> <span data-ttu-id="3582d-131">La taille de bloc la plus courante est 64 bits.</span><span class="sxs-lookup"><span data-stu-id="3582d-131">The most common block size is 64 bits.</span></span> <span data-ttu-id="3582d-132">Par exemple, est un chiffrement par bloc.</span><span class="sxs-lookup"><span data-stu-id="3582d-132">For example, DES is a block cipher.</span></span>

<span data-ttu-id="3582d-133">Voir aussi [*chiffrement de flux*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3582d-133">See also [*stream cipher*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="3582d-134"><span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**clé de chiffrement en bloc**</span><span class="sxs-lookup"><span data-stu-id="3582d-134"><span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**bulk encryption key**</span></span>
</dt> <dd>

<span data-ttu-id="3582d-135">Clé de session dérivée d’une clé principale.</span><span class="sxs-lookup"><span data-stu-id="3582d-135">A session key derived from a master key.</span></span> <span data-ttu-id="3582d-136">Les clés de chiffrement en bloc sont utilisées dans le chiffrement [*Schannel*](s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="3582d-136">Bulk encryption keys are used in [*Schannel*](s-gly.md) encryption.</span></span>

</dd> </dl>

 

 



