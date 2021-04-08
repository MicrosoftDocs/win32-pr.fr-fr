---
description: Utilisé avec les fonctions BCryptGetProperty et BCryptSetProperty pour identifier une propriété.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Identificateurs de propriété primitifs de chiffrement (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f4996a216fbc4fbf63216f99b5f630c4769e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861970"
---
# <a name="cryptography-primitive-property-identifiers"></a><span data-ttu-id="89c47-103">Identificateurs de la propriété primitive de chiffrement</span><span class="sxs-lookup"><span data-stu-id="89c47-103">Cryptography Primitive Property Identifiers</span></span>

<span data-ttu-id="89c47-104">Les valeurs suivantes sont utilisées avec les fonctions [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) et [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) pour identifier une propriété.</span><span class="sxs-lookup"><span data-stu-id="89c47-104">The following values are used with the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) and [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) functions to identify a property.</span></span>

<dl> <dt>

<span data-ttu-id="89c47-105"><span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**nom de l' \_ algorithme BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-105"><span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**BCRYPT\_ALGORITHM\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-106">L « AlgorithmName »</span><span class="sxs-lookup"><span data-stu-id="89c47-106">L"AlgorithmName"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-107">Chaîne Unicode terminée par le caractère null qui contient le nom de l’algorithme.</span><span class="sxs-lookup"><span data-stu-id="89c47-107">A null-terminated Unicode string that contains the name of the algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-108"><span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**longueur de la \_ balise d’authentification BCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-108"><span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**BCRYPT\_AUTH\_TAG\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-109">L « AuthTagLength »</span><span class="sxs-lookup"><span data-stu-id="89c47-109">L"AuthTagLength"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-110">Les longueurs d’étiquette d’authentification prises en charge par l’algorithme.</span><span class="sxs-lookup"><span data-stu-id="89c47-110">The authentication tag lengths that are supported by the algorithm.</span></span> <span data-ttu-id="89c47-111">Cette propriété est une structure de structure de [**\_ \_ \_ longueurs \_ d’authentification BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) .</span><span class="sxs-lookup"><span data-stu-id="89c47-111">This property is a [**BCRYPT\_AUTH\_TAG\_LENGTHS\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) structure.</span></span> <span data-ttu-id="89c47-112">Cette propriété s’applique uniquement aux algorithmes.</span><span class="sxs-lookup"><span data-stu-id="89c47-112">This property only applies to algorithms.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-113"><span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**\_longueur du bloc BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-113"><span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**BCRYPT\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-114">L « BlockLength »</span><span class="sxs-lookup"><span data-stu-id="89c47-114">L"BlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-115">Taille, en octets, d’un bloc de chiffrement pour l’algorithme.</span><span class="sxs-lookup"><span data-stu-id="89c47-115">The size, in bytes, of a cipher block for the algorithm.</span></span> <span data-ttu-id="89c47-116">Cette propriété s’applique uniquement aux algorithmes de chiffrement par bloc.</span><span class="sxs-lookup"><span data-stu-id="89c47-116">This property only applies to block cipher algorithms.</span></span> <span data-ttu-id="89c47-117">Ce type de données est un **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="89c47-117">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-118"><span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**\_liste des \_ tailles de bloc BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-118"><span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**BCRYPT\_BLOCK\_SIZE\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-119">L « BlockSizeList »</span><span class="sxs-lookup"><span data-stu-id="89c47-119">L"BlockSizeList"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-120">Liste des longueurs de bloc prises en charge par un algorithme de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="89c47-120">A list of the block lengths supported by an encryption algorithm.</span></span> <span data-ttu-id="89c47-121">Ce type de données est un tableau de **DWORDS**.</span><span class="sxs-lookup"><span data-stu-id="89c47-121">This data type is an array of **DWORDs**.</span></span> <span data-ttu-id="89c47-122">Le nombre d’éléments dans le tableau peut être déterminé en divisant le nombre d’octets récupérés par la taille d’une **valeur DWORD** unique.</span><span class="sxs-lookup"><span data-stu-id="89c47-122">The number of elements in the array can be determined by dividing the number of bytes retrieved by the size of a single **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-123"><span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**\_mode de chaînage \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="89c47-123"><span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**BCRYPT\_CHAINING\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-124">L « ChainingMode »</span><span class="sxs-lookup"><span data-stu-id="89c47-124">L"ChainingMode"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-125">Pointeur vers une chaîne Unicode terminée par le caractère null qui représente le mode de chaînage de l’algorithme de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="89c47-125">A pointer to a null-terminated Unicode string that represents the chaining mode of the encryption algorithm.</span></span> <span data-ttu-id="89c47-126">Cette propriété peut être définie sur un handle d’algorithme ou un handle de clé sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="89c47-126">This property can be set on an algorithm handle or a key handle to one of the following values.</span></span>



| <span data-ttu-id="89c47-127">Identificateur</span><span class="sxs-lookup"><span data-stu-id="89c47-127">Identifier</span></span>                   | <span data-ttu-id="89c47-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="89c47-128">Value</span></span>                         | <span data-ttu-id="89c47-129">Description</span><span class="sxs-lookup"><span data-stu-id="89c47-129">Description</span></span>                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c47-130">**\_mode chaîne \_ BCRYPT \_ CBC**</span><span class="sxs-lookup"><span data-stu-id="89c47-130">**BCRYPT\_CHAIN\_MODE\_CBC**</span></span> | <span data-ttu-id="89c47-131">L « ChainingModeCBC »</span><span class="sxs-lookup"><span data-stu-id="89c47-131">L"ChainingModeCBC"</span></span><br/> | <span data-ttu-id="89c47-132">Définit le mode de chaînage de l’algorithme pour [*chiffrer les chaînages de blocs*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="89c47-132">Sets the algorithm's chaining mode to [*cipher block chaining*](/windows/desktop/SecGloss/c-gly).</span></span><br/>            |
| <span data-ttu-id="89c47-133">**\_ \_ CCM en mode \_ chaîné**</span><span class="sxs-lookup"><span data-stu-id="89c47-133">**BCRYPT\_CHAIN\_MODE\_CCM**</span></span> | <span data-ttu-id="89c47-134">L « ChainingModeCCM »</span><span class="sxs-lookup"><span data-stu-id="89c47-134">L"ChainingModeCCM"</span></span><br/> | <span data-ttu-id="89c47-135">Définit le mode de chaînage de l’algorithme sur compteur avec le mode CBC-MAC (CCM). **Windows Vista :** Cette valeur est prise en charge à partir de Windows Vista avec SP1.</span><span class="sxs-lookup"><span data-stu-id="89c47-135">Sets the algorithm's chaining mode to counter with CBC-MAC mode (CCM).**Windows Vista:** This value is supported beginning with Windows Vista with SP1.</span></span><br/> <br/> |
| <span data-ttu-id="89c47-136">**\_mode de chaîne BCRYPT \_ \_ CFB**</span><span class="sxs-lookup"><span data-stu-id="89c47-136">**BCRYPT\_CHAIN\_MODE\_CFB**</span></span> | <span data-ttu-id="89c47-137">L « ChainingModeCFB »</span><span class="sxs-lookup"><span data-stu-id="89c47-137">L"ChainingModeCFB"</span></span><br/> | <span data-ttu-id="89c47-138">Définit le mode de chaînage de l’algorithme pour [*chiffrer les commentaires*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="89c47-138">Sets the algorithm's chaining mode to [*cipher feedback*](/windows/desktop/SecGloss/c-gly).</span></span><br/>                              |
| <span data-ttu-id="89c47-139">**\_ \_ BCE en mode de chaîne BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-139">**BCRYPT\_CHAIN\_MODE\_ECB**</span></span> | <span data-ttu-id="89c47-140">L « ChainingModeECB »</span><span class="sxs-lookup"><span data-stu-id="89c47-140">L"ChainingModeECB"</span></span><br/> | <span data-ttu-id="89c47-141">Définit le mode de chaînage de l’algorithme sur [*Electronic Codebook*](/windows/desktop/SecGloss/e-gly).</span><span class="sxs-lookup"><span data-stu-id="89c47-141">Sets the algorithm's chaining mode to [*electronic codebook*](/windows/desktop/SecGloss/e-gly).</span></span><br/>                  |
| <span data-ttu-id="89c47-142">**\_mode de chaîne BCRYPT \_ \_ GCM**</span><span class="sxs-lookup"><span data-stu-id="89c47-142">**BCRYPT\_CHAIN\_MODE\_GCM**</span></span> | <span data-ttu-id="89c47-143">L « ChainingModeGCM »</span><span class="sxs-lookup"><span data-stu-id="89c47-143">L"ChainingModeGCM"</span></span><br/> | <span data-ttu-id="89c47-144">Définit le mode de chaînage de l’algorithme en mode Galois/Counter (GCM). **Windows Vista :** Cette valeur est prise en charge à partir de Windows Vista avec SP1.</span><span class="sxs-lookup"><span data-stu-id="89c47-144">Sets the algorithm's chaining mode to Galois/counter mode (GCM).**Windows Vista:** This value is supported beginning with Windows Vista with SP1.</span></span><br/> <br/>       |
| <span data-ttu-id="89c47-145">**\_mode de chaîne BCRYPT \_ \_ na**</span><span class="sxs-lookup"><span data-stu-id="89c47-145">**BCRYPT\_CHAIN\_MODE\_NA**</span></span>  | <span data-ttu-id="89c47-146">L "ChainingModeN/A"</span><span class="sxs-lookup"><span data-stu-id="89c47-146">L"ChainingModeN/A"</span></span><br/> | <span data-ttu-id="89c47-147">L’algorithme ne prend pas en charge le chaînage.</span><span class="sxs-lookup"><span data-stu-id="89c47-147">The algorithm does not support chaining.</span></span><br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-148"><span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**\_paramètres BCRYPT DH \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-148"><span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**BCRYPT\_DH\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-149">L « DHParameters »</span><span class="sxs-lookup"><span data-stu-id="89c47-149">L"DHParameters"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-150">Spécifie les paramètres à utiliser avec une clé de Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="89c47-150">Specifies parameters to use with a Diffie-Hellman key.</span></span> <span data-ttu-id="89c47-151">Ce type de données est un pointeur vers une structure d' [**\_ \_ \_ en-tête de paramètre BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="89c47-151">This data type is a pointer to a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span> <span data-ttu-id="89c47-152">Cette propriété peut uniquement être définie et doit être définie pour la clé avant la fin de la clé.</span><span class="sxs-lookup"><span data-stu-id="89c47-152">This property can only be set and must be set for the key before the key is completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-153"><span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**\_paramètres du DSA de BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-153"><span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**BCRYPT\_DSA\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-154">L « DSAParameters »</span><span class="sxs-lookup"><span data-stu-id="89c47-154">L"DSAParameters"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-155">Spécifie les paramètres à utiliser avec une clé DSA.</span><span class="sxs-lookup"><span data-stu-id="89c47-155">Specifies parameters to use with a DSA key.</span></span> <span data-ttu-id="89c47-156">Cette propriété est un [**\_ \_ \_ en-tête de paramètre DSA DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) ou une structure d' [**\_ \_ \_ en-tête \_ de paramètre DSA DSA v2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) .</span><span class="sxs-lookup"><span data-stu-id="89c47-156">This property is a [**BCRYPT\_DSA\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) or a [**BCRYPT\_DSA\_PARAMETER\_HEADER\_V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) structure.</span></span> <span data-ttu-id="89c47-157">Cette propriété peut uniquement être définie et doit être définie pour la clé avant la fin de la clé.</span><span class="sxs-lookup"><span data-stu-id="89c47-157">This property can only be set and must be set for the key before the key is completed.</span></span>

<span data-ttu-id="89c47-158">**Windows 8 :** À partir de Windows 8, cette propriété peut être une structure d' [**\_ \_ \_ en \_ -tête de paramètre DSA DSA v2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) .</span><span class="sxs-lookup"><span data-stu-id="89c47-158">**Windows 8:** Beginning with Windows 8, this property can be a [**BCRYPT\_DSA\_PARAMETER\_HEADER\_V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) structure.</span></span> <span data-ttu-id="89c47-159">Utilisez cette structure si la taille de la clé dépasse 1024 bits et est inférieure ou égale à 3072 bits.</span><span class="sxs-lookup"><span data-stu-id="89c47-159">Use this structure if the key size exceeds 1024 bits and is less than or equal to 3072 bits.</span></span> <span data-ttu-id="89c47-160">Si la taille de la clé est supérieure ou égale à 512, mais inférieure ou égale à 1024 bits, utilisez la structure d' [**\_ \_ \_ en-tête de paramètre DSA DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="89c47-160">If the key size is greater than or equal to 512 but less than or equal to 1024 bits, use the [**BCRYPT\_DSA\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-161"><span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**\_longueur de \_ clé en vigueur BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-161"><span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**BCRYPT\_EFFECTIVE\_KEY\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-162">L « EffectiveKeyLength »</span><span class="sxs-lookup"><span data-stu-id="89c47-162">L"EffectiveKeyLength"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-163">Taille, en bits, de la longueur effective d’une clé RC2.</span><span class="sxs-lookup"><span data-stu-id="89c47-163">The size, in bits, of the effective length of an RC2 key.</span></span> <span data-ttu-id="89c47-164">Ce type de données est un **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="89c47-164">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-165"><span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**\_longueur du \_ bloc de hachage BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-165"><span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**BCRYPT\_HASH\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-166">L « HashBlockLength »</span><span class="sxs-lookup"><span data-stu-id="89c47-166">L"HashBlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-167">Taille, en octets, du bloc pour un hachage.</span><span class="sxs-lookup"><span data-stu-id="89c47-167">The size, in bytes, of the block for a hash.</span></span> <span data-ttu-id="89c47-168">Cette propriété s’applique uniquement aux algorithmes de hachage.</span><span class="sxs-lookup"><span data-stu-id="89c47-168">This property only applies to hash algorithms.</span></span> <span data-ttu-id="89c47-169">Ce type de données est un **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="89c47-169">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-170"><span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**\_longueur de hachage BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-170"><span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**BCRYPT\_HASH\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-171">L « HashDigestLength »</span><span class="sxs-lookup"><span data-stu-id="89c47-171">L"HashDigestLength"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-172">Taille, en octets, de la valeur de hachage d’un fournisseur de hachage.</span><span class="sxs-lookup"><span data-stu-id="89c47-172">The size, in bytes, of the hash value of a hash provider.</span></span> <span data-ttu-id="89c47-173">Ce type de données est un **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="89c47-173">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-174"><span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**\_liste d' \_ OID de hachage BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-174"><span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**BCRYPT\_HASH\_OID\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-175">L « HashOIDList »</span><span class="sxs-lookup"><span data-stu-id="89c47-175">L"HashOIDList"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-176">Liste des [*identificateurs d’objet*](/windows/desktop/SecGloss/o-gly) (OID) de hachage codé [*der*](/windows/desktop/SecGloss/d-gly).</span><span class="sxs-lookup"><span data-stu-id="89c47-176">The list of [*DER*](/windows/desktop/SecGloss/d-gly)-encoded hashing [*object identifiers*](/windows/desktop/SecGloss/o-gly) (OIDs).</span></span> <span data-ttu-id="89c47-177">Cette propriété est une structure de [**\_ \_ liste d’OID BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) .</span><span class="sxs-lookup"><span data-stu-id="89c47-177">This property is a [**BCRYPT\_OID\_LIST**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) structure.</span></span> <span data-ttu-id="89c47-178">Cette propriété peut uniquement être lue.</span><span class="sxs-lookup"><span data-stu-id="89c47-178">This property can only be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-179"><span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**\_vecteur d’initialisation de BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-179"><span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**BCRYPT\_INITIALIZATION\_VECTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-180">L "IV"</span><span class="sxs-lookup"><span data-stu-id="89c47-180">L"IV"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-181">Contient le [*vecteur d’initialisation*](/windows/desktop/SecGloss/i-gly) (IV) pour une clé.</span><span class="sxs-lookup"><span data-stu-id="89c47-181">Contains the [*initialization vector*](/windows/desktop/SecGloss/i-gly) (IV) for a key.</span></span> <span data-ttu-id="89c47-182">Cette propriété s’applique uniquement aux clés.</span><span class="sxs-lookup"><span data-stu-id="89c47-182">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-183"><span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**\_longueur de clé BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-183"><span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**BCRYPT\_KEY\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-184">L "keylength"</span><span class="sxs-lookup"><span data-stu-id="89c47-184">L"KeyLength"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-185">Taille, en bits, de la valeur de clé d’un fournisseur de clé symétrique.</span><span class="sxs-lookup"><span data-stu-id="89c47-185">The size, in bits, of the key value of a symmetric key provider.</span></span> <span data-ttu-id="89c47-186">Ce type de données est un **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="89c47-186">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-187"><span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**\_longueurs de clé BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-187"><span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**BCRYPT\_KEY\_LENGTHS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-188">L "caractères de longueur"</span><span class="sxs-lookup"><span data-stu-id="89c47-188">L"KeyLengths"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-189">Longueurs de clé prises en charge par l’algorithme.</span><span class="sxs-lookup"><span data-stu-id="89c47-189">The key lengths that are supported by the algorithm.</span></span> <span data-ttu-id="89c47-190">Cette propriété est une structure de structure de [**\_ \_ longueurs \_ de clé BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) .</span><span class="sxs-lookup"><span data-stu-id="89c47-190">This property is a [**BCRYPT\_KEY\_LENGTHS\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) structure.</span></span> <span data-ttu-id="89c47-191">Cette propriété s’applique uniquement aux algorithmes.</span><span class="sxs-lookup"><span data-stu-id="89c47-191">This property only applies to algorithms.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-192"><span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**longueur de l' \_ objet de clé BCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-192"><span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**BCRYPT\_KEY\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-193">L « KeyObjectLength »</span><span class="sxs-lookup"><span data-stu-id="89c47-193">L"KeyObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-194">Cette propriété n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="89c47-194">This property is not used.</span></span> <span data-ttu-id="89c47-195">La **propriété \_ \_ longueur de l’objet BCRYPT** est utilisée pour obtenir ces informations.</span><span class="sxs-lookup"><span data-stu-id="89c47-195">The **BCRYPT\_OBJECT\_LENGTH** property is used to obtain this information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-196"><span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**\_puissance de clé BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-196"><span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**BCRYPT\_KEY\_STRENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-197">L "KeyForce"</span><span class="sxs-lookup"><span data-stu-id="89c47-197">L"KeyStrength"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-198">Nombre de bits dans la clé.</span><span class="sxs-lookup"><span data-stu-id="89c47-198">The number of bits in the key.</span></span> <span data-ttu-id="89c47-199">Ce type de données est un **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="89c47-199">This data type is a **DWORD**.</span></span> <span data-ttu-id="89c47-200">Cette propriété s’applique uniquement aux clés.</span><span class="sxs-lookup"><span data-stu-id="89c47-200">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-201"><span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**\_longueur du \_ bloc de message BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-201"><span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**BCRYPT\_MESSAGE\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-202">L « MessageBlockLength »</span><span class="sxs-lookup"><span data-stu-id="89c47-202">L"MessageBlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-203">Cela peut être défini sur n’importe quel handle de clé pour lequel le mode de chaînage de CFB est défini.</span><span class="sxs-lookup"><span data-stu-id="89c47-203">This can be set on any key handle that has the CFB chaining mode set.</span></span> <span data-ttu-id="89c47-204">Par défaut, cette propriété a la valeur 1 pour le CFB 8 bits.</span><span class="sxs-lookup"><span data-stu-id="89c47-204">By default, this property is set to 1 for 8-bit CFB.</span></span> <span data-ttu-id="89c47-205">Si vous définissez cette valeur sur la taille de bloc en octets, vous pouvez utiliser le mode CFB de bloc complet.</span><span class="sxs-lookup"><span data-stu-id="89c47-205">Setting it to the block size in bytes causes full-block CFB to be used.</span></span> <span data-ttu-id="89c47-206">Pour les clés XTS, il est utilisé pour définir la taille, en octets, de l’unité de données XTS (généralement 512 ou 4096).</span><span class="sxs-lookup"><span data-stu-id="89c47-206">For XTS keys it is used to set the size, in bytes, of the XTS Data Unit (commonly 512 or 4096).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-207"><span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**\_longueur de plusieurs \_ objets \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="89c47-207"><span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**BCRYPT\_MULTI\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-208">L « MultiObjectLength »</span><span class="sxs-lookup"><span data-stu-id="89c47-208">L"MultiObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-209">Cette propriété retourne un [**\_ struct de \_ \_ longueur d' \_ objet multiple de BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), qui contient les informations nécessaires pour calculer la taille d’une mémoire tampon d’objet.</span><span class="sxs-lookup"><span data-stu-id="89c47-209">This property returns a [**BCRYPT\_MULTI\_OBJECT\_LENGTH\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), which contains information necessary to calculate the size of an object buffer.</span></span> <span data-ttu-id="89c47-210">Cette propriété est uniquement prise en charge sur les versions de système d’exploitation qui prennent en charge la fonction [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) .</span><span class="sxs-lookup"><span data-stu-id="89c47-210">This property is only supported on operating system versions that support the [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-211"><span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**longueur de l' \_ objet BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-211"><span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**BCRYPT\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-212">L « ObjectLength »</span><span class="sxs-lookup"><span data-stu-id="89c47-212">L"ObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-213">Taille, en octets, du sous-objet d’un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="89c47-213">The size, in bytes, of the subobject of a provider.</span></span> <span data-ttu-id="89c47-214">Ce type de données est un **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="89c47-214">This data type is a **DWORD**.</span></span> <span data-ttu-id="89c47-215">Actuellement, les fournisseurs d’algorithmes de chiffrement et de hachage symétrique utilisent des mémoires tampons allouées par l’appelant pour stocker leurs sous-objets.</span><span class="sxs-lookup"><span data-stu-id="89c47-215">Currently, the hash and symmetric cipher algorithm providers use caller-allocated buffers to store their subobjects.</span></span> <span data-ttu-id="89c47-216">Par exemple, le fournisseur de hachage vous oblige à allouer de la mémoire pour l’objet de hachage obtenu avec la fonction [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="89c47-216">For example, the hash provider requires you to allocate memory for the hash object obtained with the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span> <span data-ttu-id="89c47-217">Cette propriété fournit la taille de la mémoire tampon pour l’objet d’un fournisseur afin que vous puissiez allouer de la mémoire pour l’objet créé par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="89c47-217">This property provides the buffer size for a provider's object so you can allocate memory for the object created by the provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-218"><span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**\_schémas de remplissage \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="89c47-218"><span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**BCRYPT\_PADDING\_SCHEMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-219">L « PaddingSchemes »</span><span class="sxs-lookup"><span data-stu-id="89c47-219">L"PaddingSchemes"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-220">Représente le schéma de remplissage du fournisseur de l’algorithme RSA.</span><span class="sxs-lookup"><span data-stu-id="89c47-220">Represents the padding scheme of the RSA algorithm provider.</span></span> <span data-ttu-id="89c47-221">Ce type de données est un **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="89c47-221">This data type is a **DWORD**.</span></span> <span data-ttu-id="89c47-222">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="89c47-222">This can be one of the following values.</span></span>



| <span data-ttu-id="89c47-223">Identificateur</span><span class="sxs-lookup"><span data-stu-id="89c47-223">Identifier</span></span>                             | <span data-ttu-id="89c47-224">Valeur</span><span class="sxs-lookup"><span data-stu-id="89c47-224">Value</span></span>      | <span data-ttu-id="89c47-225">Description</span><span class="sxs-lookup"><span data-stu-id="89c47-225">Description</span></span>                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| <span data-ttu-id="89c47-226">**\_routeur de \_ Pad pris en charge par BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-226">**BCRYPT\_SUPPORTED\_PAD\_ROUTER**</span></span>     | <span data-ttu-id="89c47-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="89c47-227">0x00000001</span></span> | <span data-ttu-id="89c47-228">Le fournisseur prend en charge le remplissage ajouté par le routeur.</span><span class="sxs-lookup"><span data-stu-id="89c47-228">The provider supports padding added by the router.</span></span>         |
| <span data-ttu-id="89c47-229">**BCRYPT \_ Pad pris en charge \_ \_ PKCS1 \_ enc**</span><span class="sxs-lookup"><span data-stu-id="89c47-229">**BCRYPT\_SUPPORTED\_PAD\_PKCS1\_ENC**</span></span> | <span data-ttu-id="89c47-230">0x00000002</span><span class="sxs-lookup"><span data-stu-id="89c47-230">0x00000002</span></span> | <span data-ttu-id="89c47-231">Le fournisseur prend en charge le schéma de remplissage de chiffrement PKCS1.</span><span class="sxs-lookup"><span data-stu-id="89c47-231">The provider supports the PKCS1 encryption padding scheme.</span></span> |
| <span data-ttu-id="89c47-232">**BCRYPT \_ Supported \_ Pad \_ PKCS1 \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="89c47-232">**BCRYPT\_SUPPORTED\_PAD\_PKCS1\_SIG**</span></span> | <span data-ttu-id="89c47-233">0x00000004</span><span class="sxs-lookup"><span data-stu-id="89c47-233">0x00000004</span></span> | <span data-ttu-id="89c47-234">Le fournisseur prend en charge le schéma de remplissage de signature PKCS1.</span><span class="sxs-lookup"><span data-stu-id="89c47-234">The provider supports the PKCS1 signature padding scheme.</span></span>  |
| <span data-ttu-id="89c47-235">**BCRYPT \_ Pad pris en charge par BCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-235">**BCRYPT\_SUPPORTED\_PAD\_OAEP**</span></span>       | <span data-ttu-id="89c47-236">0x00000008</span><span class="sxs-lookup"><span data-stu-id="89c47-236">0x00000008</span></span> | <span data-ttu-id="89c47-237">Le fournisseur prend en charge le schéma de remplissage OAEP.</span><span class="sxs-lookup"><span data-stu-id="89c47-237">The provider supports the OAEP padding scheme.</span></span>             |
| <span data-ttu-id="89c47-238">**\_ \_ support technique de tapis pris en charge par BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-238">**BCRYPT\_SUPPORTED\_PAD\_PSS**</span></span>        | <span data-ttu-id="89c47-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="89c47-239">0x00000010</span></span> | <span data-ttu-id="89c47-240">Le fournisseur prend en charge le schéma de remplissage PSS.</span><span class="sxs-lookup"><span data-stu-id="89c47-240">The provider supports the PSS padding scheme.</span></span>              |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-241"><span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**\_handle du fournisseur BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-241"><span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**BCRYPT\_PROVIDER\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-242">L « ProviderHandle »</span><span class="sxs-lookup"><span data-stu-id="89c47-242">L"ProviderHandle"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-243">Handle du fournisseur CNG qui a créé l’objet passé dans le paramètre *hObject* .</span><span class="sxs-lookup"><span data-stu-id="89c47-243">The handle of the CNG provider that created the object passed in the *hObject* parameter.</span></span> <span data-ttu-id="89c47-244">Ce type de données est **une \_ \_ poignée de BCRYPT ALG**.</span><span class="sxs-lookup"><span data-stu-id="89c47-244">This data type is a **BCRYPT\_ALG\_HANDLE**.</span></span> <span data-ttu-id="89c47-245">Cette propriété peut uniquement être récupérée. elle ne peut pas être définie.</span><span class="sxs-lookup"><span data-stu-id="89c47-245">This property can only be retrieved; it cannot be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="89c47-246"><span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**longueur de la \_ signature BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="89c47-246"><span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**BCRYPT\_SIGNATURE\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89c47-247">L « SignatureLength »</span><span class="sxs-lookup"><span data-stu-id="89c47-247">L"SignatureLength"</span></span>
</dt> <dt>



<span data-ttu-id="89c47-248">Taille, en octets, de la longueur d’une signature pour une clé.</span><span class="sxs-lookup"><span data-stu-id="89c47-248">The size, in bytes, of the length of a signature for a key.</span></span> <span data-ttu-id="89c47-249">Ce type de données est un **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="89c47-249">This data type is a **DWORD**.</span></span> <span data-ttu-id="89c47-250">Cette propriété s’applique uniquement aux clés.</span><span class="sxs-lookup"><span data-stu-id="89c47-250">This property only applies to keys.</span></span> <span data-ttu-id="89c47-251">Cette propriété peut uniquement être récupérée. elle ne peut pas être définie.</span><span class="sxs-lookup"><span data-stu-id="89c47-251">This property can only be retrieved; it cannot be set.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89c47-252">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89c47-252">Requirements</span></span>



| <span data-ttu-id="89c47-253">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89c47-253">Requirement</span></span> | <span data-ttu-id="89c47-254">Valeur</span><span class="sxs-lookup"><span data-stu-id="89c47-254">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="89c47-255">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89c47-255">Minimum supported client</span></span><br/> | <span data-ttu-id="89c47-256">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89c47-256">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="89c47-257">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89c47-257">Minimum supported server</span></span><br/> | <span data-ttu-id="89c47-258">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89c47-258">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="89c47-259">En-tête</span><span class="sxs-lookup"><span data-stu-id="89c47-259">Header</span></span><br/>                   | <dl> <span data-ttu-id="89c47-260"><dt>Bcrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="89c47-260"><dt>Bcrypt.h</dt></span></span> </dl> |



 

