---
description: Utilisé pour identifier une propriété de stockage de clé.
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: Identificateurs de propriété de stockage de clés (ncrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 813a15ba106989cb558eba181bc893d75c6d1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538206"
---
# <a name="key-storage-property-identifiers"></a><span data-ttu-id="9dedc-103">Identificateurs de propriété de stockage de clés</span><span class="sxs-lookup"><span data-stu-id="9dedc-103">Key Storage Property Identifiers</span></span>

<span data-ttu-id="9dedc-104">Les valeurs suivantes sont utilisées pour identifier une propriété de stockage de clé.</span><span class="sxs-lookup"><span data-stu-id="9dedc-104">The following values are used to identify a key storage property.</span></span>

<dl> <dt>

<span data-ttu-id="9dedc-105"><span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**\_propriété du groupe d’algorithmes NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-105"><span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**NCRYPT\_ALGORITHM\_GROUP\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-106">L "groupe d’algorithmes"</span><span class="sxs-lookup"><span data-stu-id="9dedc-106">L"Algorithm Group"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-107">Chaîne Unicode terminée par le caractère null qui contient le nom du groupe d’algorithmes de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9dedc-107">A null-terminated Unicode string that contains the name of the object's algorithm group.</span></span> <span data-ttu-id="9dedc-108">Cette propriété s’applique uniquement aux clés.</span><span class="sxs-lookup"><span data-stu-id="9dedc-108">This property only applies to keys.</span></span> <span data-ttu-id="9dedc-109">Les identificateurs suivants sont retournés par le fournisseur de stockage de clés Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9dedc-109">The following identifiers are returned by the Microsoft key storage provider.</span></span>



| <span data-ttu-id="9dedc-110">Identificateur</span><span class="sxs-lookup"><span data-stu-id="9dedc-110">Identifier</span></span>                                     | <span data-ttu-id="9dedc-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dedc-111">Value</span></span>              | <span data-ttu-id="9dedc-112">Description</span><span class="sxs-lookup"><span data-stu-id="9dedc-112">Description</span></span>                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| <span data-ttu-id="9dedc-113">**\_groupe d' \_ algorithmes de RSA NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-113">**NCRYPT\_RSA\_ALGORITHM\_GROUP**</span></span><br/>   | <span data-ttu-id="9dedc-114">DOTÉ</span><span class="sxs-lookup"><span data-stu-id="9dedc-114">"RSA"</span></span><br/>   | <span data-ttu-id="9dedc-115">Groupe d’algorithmes RSA.</span><span class="sxs-lookup"><span data-stu-id="9dedc-115">The RSA algorithm group.</span></span><br/>                           |
| <span data-ttu-id="9dedc-116">**\_groupe d' \_ algorithmes de DH \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-116">**NCRYPT\_DH\_ALGORITHM\_GROUP**</span></span><br/>    | <span data-ttu-id="9dedc-117">VA</span><span class="sxs-lookup"><span data-stu-id="9dedc-117">"DH"</span></span><br/>    | <span data-ttu-id="9dedc-118">Groupe d’algorithmes Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="9dedc-118">The Diffie-Hellman algorithm group.</span></span><br/>                |
| <span data-ttu-id="9dedc-119">**\_groupe d' \_ algorithmes DSA NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-119">**NCRYPT\_DSA\_ALGORITHM\_GROUP**</span></span><br/>   | <span data-ttu-id="9dedc-120">DSA</span><span class="sxs-lookup"><span data-stu-id="9dedc-120">"DSA"</span></span><br/>   | <span data-ttu-id="9dedc-121">Groupe d’algorithmes DSA.</span><span class="sxs-lookup"><span data-stu-id="9dedc-121">The DSA algorithm group.</span></span><br/>                           |
| <span data-ttu-id="9dedc-122">**\_groupe d' \_ algorithmes ECDSA NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-122">**NCRYPT\_ECDSA\_ALGORITHM\_GROUP**</span></span><br/> | <span data-ttu-id="9dedc-123">ECDsa</span><span class="sxs-lookup"><span data-stu-id="9dedc-123">"ECDSA"</span></span><br/> | <span data-ttu-id="9dedc-124">Groupe d’algorithmes DSA de la courbe elliptique.</span><span class="sxs-lookup"><span data-stu-id="9dedc-124">The elliptic curve DSA algorithm group.</span></span><br/>            |
| <span data-ttu-id="9dedc-125">**\_groupe d' \_ algorithmes ECDH NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-125">**NCRYPT\_ECDH\_ALGORITHM\_GROUP**</span></span><br/>  | <span data-ttu-id="9dedc-126">ECDH</span><span class="sxs-lookup"><span data-stu-id="9dedc-126">"ECDH"</span></span><br/>  | <span data-ttu-id="9dedc-127">Le groupe d’algorithmes Diffie-Hellman de courbe elliptique.</span><span class="sxs-lookup"><span data-stu-id="9dedc-127">The elliptic curve Diffie-Hellman algorithm group.</span></span><br/> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-128"><span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**\_propriété d’algorithme NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-128"><span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**NCRYPT\_ALGORITHM\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-129">L "nom de l’algorithme"</span><span class="sxs-lookup"><span data-stu-id="9dedc-129">L"Algorithm Name"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-130">Chaîne Unicode terminée par le caractère null qui contient le nom de l’algorithme de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9dedc-130">A null-terminated Unicode string that contains the name of the object's algorithm.</span></span> <span data-ttu-id="9dedc-131">Il peut s’agir de l’un des [**identificateurs d’algorithme CNG**](cng-algorithm-identifiers.md) prédéfinis ou d’un autre identificateur d’algorithme inscrit.</span><span class="sxs-lookup"><span data-stu-id="9dedc-131">This can be one of the predefined [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) or another registered algorithm identifier.</span></span> <span data-ttu-id="9dedc-132">Cette propriété s’applique uniquement aux clés.</span><span class="sxs-lookup"><span data-stu-id="9dedc-132">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-133"><span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**\_clé ECDH associée à NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-133"><span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**NCRYPT\_ASSOCIATED\_ECDH\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-134">L « SmartCardAssociatedECDHKey »</span><span class="sxs-lookup"><span data-stu-id="9dedc-134">L"SmartCardAssociatedECDHKey"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-135">Valeur **LPWStr** qui indique le nom de conteneur de la clé ECDH (elliptic Curve Diffie-Hellman) à utiliser lors de l’ouverture de session pour un handle donné à une clé ECDSA (Elliptic Curve Digital Signature Algorithm).</span><span class="sxs-lookup"><span data-stu-id="9dedc-135">An **LPWSTR** value that indicates the container name of the Elliptic Curve Diffie-Hellman (ECDH) key to use during logon for a given handle to an Elliptic Curve Digital Signature Algorithm (ECDSA) key.</span></span> <span data-ttu-id="9dedc-136">S’il n’existe aucune clé ECDH sur la carte, le [*fournisseur de stockage de clés*](/windows/desktop/SecGloss/k-gly) (KSP) retourne le NPD est **\_ \_ introuvable**.</span><span class="sxs-lookup"><span data-stu-id="9dedc-136">If there are no ECDH keys on the card, the [*key storage provider*](/windows/desktop/SecGloss/k-gly) (KSP) returns **NTE\_NOT\_FOUND**.</span></span> <span data-ttu-id="9dedc-137">Cette propriété s’applique aux clés ECDSA pour l’ouverture de session avec les cartes à puce.</span><span class="sxs-lookup"><span data-stu-id="9dedc-137">This property applies to ECDSA keys for logon with smart cards.</span></span> <span data-ttu-id="9dedc-138">La propriété est prise en charge par le fournisseur de stockage de clés de carte à puce Microsoft et non par le fournisseur de stockage de clés logicielles Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9dedc-138">The property is supported by the Microsoft Smart Card key storage provider and not by the Microsoft Software key storage provider.</span></span>

<span data-ttu-id="9dedc-139">**Windows Server 2008 et Windows Vista :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9dedc-139">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-140"><span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**\_propriété de \_ longueur de bloc NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-140"><span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**NCRYPT\_BLOCK\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-141">L "longueur du bloc"</span><span class="sxs-lookup"><span data-stu-id="9dedc-141">L"Block Length"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-142">**Valeur DWORD** qui contient la longueur, en octets, du bloc de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9dedc-142">A **DWORD** that contains the length, in bytes, of the encryption block.</span></span> <span data-ttu-id="9dedc-143">Cette propriété s’applique uniquement aux clés qui prennent en charge le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9dedc-143">This property only applies to keys that support encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-144"><span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**\_propriété du certificat NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-144"><span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**NCRYPT\_CERTIFICATE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-145">L « SmartCardKeyCertificate »</span><span class="sxs-lookup"><span data-stu-id="9dedc-145">L"SmartCardKeyCertificate"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-146">[*Objet BLOB*](/windows/desktop/SecGloss/b-gly) qui contient un certificat X. 509 associé à la clé.</span><span class="sxs-lookup"><span data-stu-id="9dedc-146">A [*BLOB*](/windows/desktop/SecGloss/b-gly) that contains an X.509 certificate that is associated with the key.</span></span>

<span data-ttu-id="9dedc-147">**Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** [*Objet BLOB*](/windows/desktop/SecGloss/b-gly) qui contient le [*certificat*](/windows/desktop/SecGloss/c-gly)de clé de [*carte à puce*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="9dedc-147">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** A [*BLOB*](/windows/desktop/SecGloss/b-gly) that contains the [*smart card*](/windows/desktop/SecGloss/s-gly) key [*certificate*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="9dedc-148">Cette propriété n’est pas prise en charge par le fournisseur de stockage de clés logicielles Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9dedc-148">This property is not supported by the Microsoft Software Key Storage Provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-149"><span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**\_propriété des \_ paramètres NCRYPT DH \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-149"><span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**NCRYPT\_DH\_PARAMETERS\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-150">L « DHParameters »</span><span class="sxs-lookup"><span data-stu-id="9dedc-150">L"DHParameters"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-151">Spécifie les paramètres à utiliser avec une clé de Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="9dedc-151">Specifies parameters to use with a Diffie-Hellman key.</span></span> <span data-ttu-id="9dedc-152">Ce type de données est un pointeur vers une structure d' [**\_ \_ \_ en-tête de paramètre BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="9dedc-152">This data type is a pointer to a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span> <span data-ttu-id="9dedc-153">Cette propriété peut uniquement être définie et doit être définie pour la clé avant la fin de la clé.</span><span class="sxs-lookup"><span data-stu-id="9dedc-153">This property can only be set and must be set for the key before the key is completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-154"><span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**propriété de la \_ stratégie d’exportation NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-154"><span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**NCRYPT\_EXPORT\_POLICY\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-155">L « stratégie d’exportation »</span><span class="sxs-lookup"><span data-stu-id="9dedc-155">L"Export Policy"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-156">Valeur **DWORD** qui contient un jeu d’indicateurs qui spécifient la stratégie d’exportation pour une clé rendue persistante.</span><span class="sxs-lookup"><span data-stu-id="9dedc-156">A **DWORD** that contains a set of flags that specify the export policy for a persisted key.</span></span> <span data-ttu-id="9dedc-157">Cette propriété s’applique uniquement aux clés.</span><span class="sxs-lookup"><span data-stu-id="9dedc-157">This property only applies to keys.</span></span> <span data-ttu-id="9dedc-158">Il peut contenir zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9dedc-158">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="9dedc-159">Identificateur</span><span class="sxs-lookup"><span data-stu-id="9dedc-159">Identifier</span></span>                                    | <span data-ttu-id="9dedc-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dedc-160">Value</span></span>      | <span data-ttu-id="9dedc-161">Description</span><span class="sxs-lookup"><span data-stu-id="9dedc-161">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dedc-162">**NCRYPT- \_ autoriser l' \_ indicateur d’exportation \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-162">**NCRYPT\_ALLOW\_EXPORT\_FLAG**</span></span>               | <span data-ttu-id="9dedc-163">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9dedc-163">0x00000001</span></span> | <span data-ttu-id="9dedc-164">La clé privée peut être exportée.</span><span class="sxs-lookup"><span data-stu-id="9dedc-164">The private key can be exported.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9dedc-165">**NCRYPT \_ autoriser \_ l' \_ indicateur d’exportation en texte clair \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-165">**NCRYPT\_ALLOW\_PLAINTEXT\_EXPORT\_FLAG**</span></span>    | <span data-ttu-id="9dedc-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9dedc-166">0x00000002</span></span> | <span data-ttu-id="9dedc-167">La clé privée peut être exportée sous forme de texte en clair.</span><span class="sxs-lookup"><span data-stu-id="9dedc-167">The private key can be exported in plaintext form.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="9dedc-168">**\_ \_ l’indicateur d’archivage d’autorisation NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-168">**NCRYPT\_ALLOW\_ARCHIVING\_FLAG**</span></span>            | <span data-ttu-id="9dedc-169">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9dedc-169">0x00000004</span></span> | <span data-ttu-id="9dedc-170">La clé privée peut être exportée une fois à des fins d’archivage.</span><span class="sxs-lookup"><span data-stu-id="9dedc-170">The private key can be exported once for archiving purposes.</span></span> <span data-ttu-id="9dedc-171">Cet indicateur s’applique uniquement au handle de clé d’origine sur lequel il est défini.</span><span class="sxs-lookup"><span data-stu-id="9dedc-171">This flag only applies to the original key handle on which it is set.</span></span> <span data-ttu-id="9dedc-172">Cette stratégie ne peut être appliquée qu’au handle de clé d’origine.</span><span class="sxs-lookup"><span data-stu-id="9dedc-172">This policy can only be applied to the original key handle.</span></span> <span data-ttu-id="9dedc-173">Une fois le descripteur de clé fermé, la clé ne peut plus être exportée à des fins d’archivage.</span><span class="sxs-lookup"><span data-stu-id="9dedc-173">After the key handle has been closed, the key can no longer be exported for archiving purposes.</span></span>                   |
| <span data-ttu-id="9dedc-174">**NCRYPT \_ autoriser \_ \_ l’indicateur d’archivage en texte clair \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-174">**NCRYPT\_ALLOW\_PLAINTEXT\_ARCHIVING\_FLAG**</span></span> | <span data-ttu-id="9dedc-175">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9dedc-175">0x00000008</span></span> | <span data-ttu-id="9dedc-176">La clé privée peut être exportée une seule fois sous forme de texte en clair à des fins d’archivage.</span><span class="sxs-lookup"><span data-stu-id="9dedc-176">The private key can be exported once in plaintext form for archiving purposes.</span></span> <span data-ttu-id="9dedc-177">Cet indicateur s’applique uniquement au handle de clé d’origine sur lequel il est défini.</span><span class="sxs-lookup"><span data-stu-id="9dedc-177">This flag only applies to the original key handle on which it is set.</span></span> <span data-ttu-id="9dedc-178">Cette stratégie ne peut être appliquée qu’au handle de clé d’origine.</span><span class="sxs-lookup"><span data-stu-id="9dedc-178">This policy can only be applied to the original key handle.</span></span> <span data-ttu-id="9dedc-179">Une fois le descripteur de clé fermé, la clé ne peut plus être exportée à des fins d’archivage.</span><span class="sxs-lookup"><span data-stu-id="9dedc-179">After the key handle has been closed, the key can no longer be exported for archiving purposes.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-180"><span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**\_propriété de \_ type impl impl \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-180"><span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**NCRYPT\_IMPL\_TYPE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-181">L "type impl"</span><span class="sxs-lookup"><span data-stu-id="9dedc-181">L"Impl Type"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-182">Valeur **DWORD** qui contient un jeu d’indicateurs qui définissent les détails d’implémentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9dedc-182">A **DWORD** that contains a set of flags that define implementation details of the provider.</span></span> <span data-ttu-id="9dedc-183">Cette propriété s’applique uniquement aux fournisseurs de stockage de clés.</span><span class="sxs-lookup"><span data-stu-id="9dedc-183">This property only applies to key storage providers.</span></span> <span data-ttu-id="9dedc-184">Il peut contenir zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9dedc-184">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="9dedc-185">Identificateur</span><span class="sxs-lookup"><span data-stu-id="9dedc-185">Identifier</span></span>                            | <span data-ttu-id="9dedc-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dedc-186">Value</span></span>      | <span data-ttu-id="9dedc-187">Description</span><span class="sxs-lookup"><span data-stu-id="9dedc-187">Description</span></span>                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| <span data-ttu-id="9dedc-188">**\_ \_ indicateur matériel de NCRYPT impl \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-188">**NCRYPT\_IMPL\_HARDWARE\_FLAG**</span></span>      | <span data-ttu-id="9dedc-189">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9dedc-189">0x00000001</span></span> | <span data-ttu-id="9dedc-190">Le fournisseur est basé sur le matériel.</span><span class="sxs-lookup"><span data-stu-id="9dedc-190">The provider is hardware based.</span></span>                           |
| <span data-ttu-id="9dedc-191">**\_indicateur du \_ logiciel NCRYPT impl \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-191">**NCRYPT\_IMPL\_SOFTWARE\_FLAG**</span></span>      | <span data-ttu-id="9dedc-192">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9dedc-192">0x00000002</span></span> | <span data-ttu-id="9dedc-193">Le fournisseur est basé sur un logiciel.</span><span class="sxs-lookup"><span data-stu-id="9dedc-193">The provider is software based.</span></span>                           |
| <span data-ttu-id="9dedc-194">**\_indicateur de \_ déstockage du impl impl \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-194">**NCRYPT\_IMPL\_REMOVABLE\_FLAG**</span></span>     | <span data-ttu-id="9dedc-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9dedc-195">0x00000008</span></span> | <span data-ttu-id="9dedc-196">Le fournisseur est amovible.</span><span class="sxs-lookup"><span data-stu-id="9dedc-196">The provider is removable.</span></span>                                |
| <span data-ttu-id="9dedc-197">**\_indicateur de \_ \_ RNG matériel \_ de NCRYPT impl**</span><span class="sxs-lookup"><span data-stu-id="9dedc-197">**NCRYPT\_IMPL\_HARDWARE\_RNG\_FLAG**</span></span> | <span data-ttu-id="9dedc-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9dedc-198">0x00000010</span></span> | <span data-ttu-id="9dedc-199">Le fournisseur est un générateur de nombres aléatoires basé sur le matériel.</span><span class="sxs-lookup"><span data-stu-id="9dedc-199">The provider is a hardware based random number generator.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-200"><span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**\_ \_ propriété type de clé NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-200"><span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**NCRYPT\_KEY\_TYPE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-201">L "type de clé"</span><span class="sxs-lookup"><span data-stu-id="9dedc-201">L"Key Type"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-202">Valeur **DWORD** qui contient un jeu d’indicateurs qui définissent le type de clé.</span><span class="sxs-lookup"><span data-stu-id="9dedc-202">A **DWORD** that contains a set of flags that define the key type.</span></span> <span data-ttu-id="9dedc-203">Cette propriété s’applique uniquement aux clés.</span><span class="sxs-lookup"><span data-stu-id="9dedc-203">This property only applies to keys.</span></span> <span data-ttu-id="9dedc-204">Il peut contenir zéro ou la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="9dedc-204">This can contain zero or the following value.</span></span>



| <span data-ttu-id="9dedc-205">Identificateur</span><span class="sxs-lookup"><span data-stu-id="9dedc-205">Identifier</span></span>                     | <span data-ttu-id="9dedc-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dedc-206">Value</span></span>      | <span data-ttu-id="9dedc-207">Description</span><span class="sxs-lookup"><span data-stu-id="9dedc-207">Description</span></span>                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dedc-208">**\_indicateur de \_ clé d’ordinateur NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-208">**NCRYPT\_MACHINE\_KEY\_FLAG**</span></span> | <span data-ttu-id="9dedc-209">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9dedc-209">0x00000001</span></span> | <span data-ttu-id="9dedc-210">La clé s’applique à l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="9dedc-210">The key applies to the local computer.</span></span> <span data-ttu-id="9dedc-211">Si cet indicateur n’est pas présent, la clé s’applique à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="9dedc-211">If this flag is not present, the key applies to the current user.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-212"><span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**propriété d’utilisation de la \_ clé NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-212"><span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**NCRYPT\_KEY\_USAGE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-213">L "utilisation de la clé"</span><span class="sxs-lookup"><span data-stu-id="9dedc-213">L"Key Usage"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-214">Valeur **DWORD** qui contient un jeu d’indicateurs qui définissent les détails d’utilisation d’une clé.</span><span class="sxs-lookup"><span data-stu-id="9dedc-214">A **DWORD** that contains a set of flags that define the usage details for a key.</span></span> <span data-ttu-id="9dedc-215">Cette propriété s’applique uniquement aux clés.</span><span class="sxs-lookup"><span data-stu-id="9dedc-215">This property only applies to keys.</span></span> <span data-ttu-id="9dedc-216">Il peut contenir zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9dedc-216">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="9dedc-217">Identificateur</span><span class="sxs-lookup"><span data-stu-id="9dedc-217">Identifier</span></span>                              | <span data-ttu-id="9dedc-218">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dedc-218">Value</span></span>      | <span data-ttu-id="9dedc-219">Description</span><span class="sxs-lookup"><span data-stu-id="9dedc-219">Description</span></span>                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| <span data-ttu-id="9dedc-220">**NCRYPT \_ autoriser le \_ déchiffrement \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-220">**NCRYPT\_ALLOW\_DECRYPT\_FLAG**</span></span>        | <span data-ttu-id="9dedc-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9dedc-221">0x00000001</span></span> | <span data-ttu-id="9dedc-222">La clé peut être utilisée pour le déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="9dedc-222">The key can be used for decryption.</span></span>                  |
| <span data-ttu-id="9dedc-223">**NCRYPT \_ autoriser \_ l' \_ indicateur de signature**</span><span class="sxs-lookup"><span data-stu-id="9dedc-223">**NCRYPT\_ALLOW\_SIGNING\_FLAG**</span></span>        | <span data-ttu-id="9dedc-224">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9dedc-224">0x00000002</span></span> | <span data-ttu-id="9dedc-225">La clé peut être utilisée pour la signature.</span><span class="sxs-lookup"><span data-stu-id="9dedc-225">The key can be used for signing.</span></span>                     |
| <span data-ttu-id="9dedc-226">**\_indicateur d' \_ accord de clé d’autorisation NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-226">**NCRYPT\_ALLOW\_KEY\_AGREEMENT\_FLAG**</span></span> | <span data-ttu-id="9dedc-227">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9dedc-227">0x00000004</span></span> | <span data-ttu-id="9dedc-228">La clé peut être utilisée pour le chiffrement de l’accord secret.</span><span class="sxs-lookup"><span data-stu-id="9dedc-228">The key can be used for secret agreement encryption.</span></span> |
| <span data-ttu-id="9dedc-229">**NCRYPT \_ autoriser \_ toutes les \_ utilisations**</span><span class="sxs-lookup"><span data-stu-id="9dedc-229">**NCRYPT\_ALLOW\_ALL\_USAGES**</span></span>          | <span data-ttu-id="9dedc-230">0x00ffffff</span><span class="sxs-lookup"><span data-stu-id="9dedc-230">0x00ffffff</span></span> | <span data-ttu-id="9dedc-231">La clé peut être utilisée dans n’importe quel but.</span><span class="sxs-lookup"><span data-stu-id="9dedc-231">The key can be used for any purpose.</span></span>                 |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-232"><span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**propriété de la \_ dernière \_ modification de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-232"><span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**NCRYPT\_LAST\_MODIFIED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-233">L "modifié"</span><span class="sxs-lookup"><span data-stu-id="9dedc-233">L"Modified"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-234">Indique le moment où la clé a été modifiée pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="9dedc-234">Indicates when the key was last modified.</span></span> <span data-ttu-id="9dedc-235">Ce type de données est un pointeur vers une structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="9dedc-235">This data type is a pointer to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure.</span></span> <span data-ttu-id="9dedc-236">Cette propriété s’applique uniquement aux clés persistantes.</span><span class="sxs-lookup"><span data-stu-id="9dedc-236">This property only applies to persisted keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-237"><span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**\_propriété de longueur NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-237"><span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**NCRYPT\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-238">L "longueur"</span><span class="sxs-lookup"><span data-stu-id="9dedc-238">L"Length"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-239">**Valeur DWORD** qui contient la longueur, en bits, de la clé.</span><span class="sxs-lookup"><span data-stu-id="9dedc-239">A **DWORD** that contains the length, in bits, of the key.</span></span> <span data-ttu-id="9dedc-240">Cette propriété s’applique uniquement aux clés.</span><span class="sxs-lookup"><span data-stu-id="9dedc-240">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-241"><span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**\_propriété de longueurs NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-241"><span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**NCRYPT\_LENGTHS\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-242">L « longueurs »</span><span class="sxs-lookup"><span data-stu-id="9dedc-242">L"Lengths"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-243">Indique les tailles de clé prises en charge par la clé.</span><span class="sxs-lookup"><span data-stu-id="9dedc-243">Indicates the key sizes that are supported by the key.</span></span> <span data-ttu-id="9dedc-244">Ce type de données est un pointeur vers une structure de [**\_ \_ longueurs pris en charge par NCRYPT**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) qui contient ces informations.</span><span class="sxs-lookup"><span data-stu-id="9dedc-244">This data type is a pointer to an [**NCRYPT\_SUPPORTED\_LENGTHS**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) structure that contains this information.</span></span> <span data-ttu-id="9dedc-245">Cette propriété s’applique uniquement aux clés.</span><span class="sxs-lookup"><span data-stu-id="9dedc-245">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-246"><span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**\_propriété de longueur maximale du \_ nom NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-246"><span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**NCRYPT\_MAX\_NAME\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-247">L "longueur maximale du nom"</span><span class="sxs-lookup"><span data-stu-id="9dedc-247">L"Max Name Length"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-248">**Valeur DWORD** qui contient la longueur maximale, en caractères, du nom d’une clé persistante.</span><span class="sxs-lookup"><span data-stu-id="9dedc-248">A **DWORD** that contains the maximum length, in characters, of the name of a persistent key.</span></span> <span data-ttu-id="9dedc-249">Cette propriété s’applique uniquement à un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9dedc-249">This property only applies to a provider.</span></span>

<span data-ttu-id="9dedc-250">Cette propriété est principalement destinée à être utilisée par des fournisseurs de stockage de clés qui stockent leurs clés sur un appareil disposant d’une quantité limitée de mémoire disponible, telle qu’une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="9dedc-250">This property is primarily intended to be used by key storage providers that store their keys on a device that has a limited amount of available memory, such as a smart card.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-251"><span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**\_propriété de nom NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-251"><span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**NCRYPT\_NAME\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-252">L "nom"</span><span class="sxs-lookup"><span data-stu-id="9dedc-252">L"Name"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-253">Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9dedc-253">A pointer to a null-terminated Unicode string that contains the name of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-254"><span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**propriété de l' \_ invite du pin NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-254"><span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**NCRYPT\_PIN\_PROMPT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-255">L « SmartCardPinPrompt »</span><span class="sxs-lookup"><span data-stu-id="9dedc-255">L"SmartCardPinPrompt"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-256">Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9dedc-256">This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-257"><span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**\_propriété du pin NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-257"><span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**NCRYPT\_PIN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-258">L « SmartCardPin »</span><span class="sxs-lookup"><span data-stu-id="9dedc-258">L"SmartCardPin"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-259">Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="9dedc-259">A pointer to a null-terminated Unicode string that contains the PIN.</span></span> <span data-ttu-id="9dedc-260">Le code PIN est utilisé pour une clé de carte à puce ou le mot de passe pour une clé protégée par mot de passe stockée dans un KSP basé sur logiciel.</span><span class="sxs-lookup"><span data-stu-id="9dedc-260">The PIN is used for a smart card key or the password for a password-protected key stored in a software-based KSP.</span></span> <span data-ttu-id="9dedc-261">Cette propriété ne peut être définie que.</span><span class="sxs-lookup"><span data-stu-id="9dedc-261">This property can only be set.</span></span> <span data-ttu-id="9dedc-262">Microsoft KSP met en cache cette valeur afin que l’utilisateur ne soit invité qu’une seule fois par processus.</span><span class="sxs-lookup"><span data-stu-id="9dedc-262">Microsoft KSPs will cache this value so that the user is only prompted once per process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-263"><span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**\_propriété du \_ handle du fournisseur NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-263"><span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**NCRYPT\_PROVIDER\_HANDLE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-264">L "handle du fournisseur"</span><span class="sxs-lookup"><span data-stu-id="9dedc-264">L"Provider Handle"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-265">Un **\_ \_ handle NCRYPT Prov** qui contient le descripteur du fournisseur de stockage de clés CNG.</span><span class="sxs-lookup"><span data-stu-id="9dedc-265">An **NCRYPT\_PROV\_HANDLE** that contains the handle of the CNG key storage provider.</span></span> <span data-ttu-id="9dedc-266">Lorsque vous avez terminé d’utiliser le handle, vous devez appeler [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) pour le libérer.</span><span class="sxs-lookup"><span data-stu-id="9dedc-266">When you are finished using the handle, you must call [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) to release it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-267"><span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**\_propriété de lecteur NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-267"><span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**NCRYPT\_READER\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-268">L « SmartCardReader »</span><span class="sxs-lookup"><span data-stu-id="9dedc-268">L"SmartCardReader"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-269">Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le nom du lecteur de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="9dedc-269">A pointer to a null-terminated Unicode string that contains the name of the smart card reader.</span></span> <span data-ttu-id="9dedc-270">Cette propriété ne peut être définie que.</span><span class="sxs-lookup"><span data-stu-id="9dedc-270">This property can only be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-271"><span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**\_ \_ propriété CERTSTORE racine \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="9dedc-271"><span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**NCRYPT\_ROOT\_CERTSTORE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-272">L « SmartcardRootCertStore »</span><span class="sxs-lookup"><span data-stu-id="9dedc-272">L"SmartcardRootCertStore"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-273">**HCERTSTORE** qui représente le magasin de certificats racines de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="9dedc-273">An **HCERTSTORE** that represents the smart card root certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-274"><span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCRYPT \_ \_ \_ ID PIN cicatrice**</span><span class="sxs-lookup"><span data-stu-id="9dedc-274"><span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span> **NCRYPT\_SCARD\_PIN\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-275">L « SmartCardPinId »</span><span class="sxs-lookup"><span data-stu-id="9dedc-275">L"SmartCardPinId"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-276">Pointeur vers la valeur **d' \_ ID de code confidentiel** associée à une [*clé de chiffrement*](/windows/desktop/SecGloss/c-gly) donnée sur une [*carte à puce*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="9dedc-276">A pointer to the **PIN\_ID** value associated with a given [*cryptographic key*](/windows/desktop/SecGloss/c-gly) on a [*smart card*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="9dedc-277">Il s’agit d’une propriété en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9dedc-277">This is a read-only property.</span></span> <span data-ttu-id="9dedc-278">Le type de données de l' **\_ ID de code confidentiel** est défini dans cardmod. h.</span><span class="sxs-lookup"><span data-stu-id="9dedc-278">The **PIN\_ID** data type is defined in Cardmod.h.</span></span>

<span data-ttu-id="9dedc-279">**Windows Server 2008 et Windows Vista :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9dedc-279">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-280"><span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**\_informations de pin cicatrices NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-280"><span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**NCRYPT\_SCARD\_PIN\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-281">L « SmartCardPinInfo »</span><span class="sxs-lookup"><span data-stu-id="9dedc-281">L"SmartCardPinInfo"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-282">Pointeur désignant la structure d' [**\_ informations**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) du code confidentiel associé à une clé de chiffrement donnée sur la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="9dedc-282">A pointer to [**PIN\_INFO**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) structure of the PIN associated with a given cryptographic key on the smart card.</span></span> <span data-ttu-id="9dedc-283">L’appelant fournit le handle de clé.</span><span class="sxs-lookup"><span data-stu-id="9dedc-283">The caller provides the key handle.</span></span> <span data-ttu-id="9dedc-284">Cette propriété est une propriété en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9dedc-284">This property is a read-only property.</span></span> <span data-ttu-id="9dedc-285">La structure d' **\_ informations sur le code confidentiel** est définie dans cardmod. h.</span><span class="sxs-lookup"><span data-stu-id="9dedc-285">The **PIN\_INFO** structure is defined in Cardmod.h.</span></span>

<span data-ttu-id="9dedc-286">**Windows Server 2008 et Windows Vista :** Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9dedc-286">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-287"><span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**\_propriété de \_ code confidentiel sécurisé NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-287"><span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**NCRYPT\_SECURE\_PIN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-288">L « SmartCardSecurePin »</span><span class="sxs-lookup"><span data-stu-id="9dedc-288">L"SmartCardSecurePin"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-289">Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le code confidentiel de la session de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="9dedc-289">A pointer to a null-terminated Unicode string that contains the smart card session PIN.</span></span> <span data-ttu-id="9dedc-290">Cette propriété ne peut être définie que.</span><span class="sxs-lookup"><span data-stu-id="9dedc-290">This property can only be set.</span></span>

<span data-ttu-id="9dedc-291">**Windows Vista :** Cette propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9dedc-291">**Windows Vista:** This property is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-292"><span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**propriété de la description de la \_ sécurité NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-292"><span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**NCRYPT\_SECURITY\_DESCR\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-293">L "descr de sécurité"</span><span class="sxs-lookup"><span data-stu-id="9dedc-293">L"Security Descr"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-294">Pointeur vers une structure [**de \_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) qui contient des informations de contrôle d’accès pour la clé.</span><span class="sxs-lookup"><span data-stu-id="9dedc-294">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains access control information for the key.</span></span> <span data-ttu-id="9dedc-295">Cette propriété s’applique uniquement aux clés persistantes.</span><span class="sxs-lookup"><span data-stu-id="9dedc-295">This property only applies to persistent keys.</span></span> <span data-ttu-id="9dedc-296">Le paramètre *dwFlags* de la fonction [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) ou [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) identifie la partie du descripteur de sécurité à récupérer ou à définir.</span><span class="sxs-lookup"><span data-stu-id="9dedc-296">The *dwFlags* parameter of the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) or [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) function identifies the part of the security descriptor to get or set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-297"><span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**\_propriété de \_ \_ prise en charge \_ de la description de la sécurité NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="9dedc-297"><span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**NCRYPT\_SECURITY\_DESCR\_SUPPORT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-298">L « prise en charge de descr de sécurité »</span><span class="sxs-lookup"><span data-stu-id="9dedc-298">L"Security Descr Support"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-299">Indique si le fournisseur prend en charge les descripteurs de sécurité pour les clés.</span><span class="sxs-lookup"><span data-stu-id="9dedc-299">Indicates whether the provider supports security descriptors for keys.</span></span> <span data-ttu-id="9dedc-300">Cette propriété est une **valeur DWORD** qui contient 1 si le fournisseur prend en charge les descripteurs de sécurité pour les clés.</span><span class="sxs-lookup"><span data-stu-id="9dedc-300">This property is a **DWORD** that contains 1 if the provider supports security descriptors for keys.</span></span> <span data-ttu-id="9dedc-301">Si cette propriété contient une autre valeur, ou si la fonction [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) retourne **NPD \_ non \_ pris en charge**, le fournisseur ne prend pas en charge les descripteurs de sécurité pour les clés.</span><span class="sxs-lookup"><span data-stu-id="9dedc-301">If this property contains any other value, or if the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function returns **NTE\_NOT\_SUPPORTED**, then the provider does not support security descriptors for keys.</span></span> <span data-ttu-id="9dedc-302">Cette propriété s’applique uniquement aux fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="9dedc-302">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-303"><span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**\_ \_ propriété GUID de la carte à puce NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-303"><span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**NCRYPT\_SMARTCARD\_GUID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-304">L « SmartCardGuid »</span><span class="sxs-lookup"><span data-stu-id="9dedc-304">L"SmartCardGuid"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-305">Objet BLOB qui contient l’identificateur de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="9dedc-305">A BLOB that contains the identifier of the smart card.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-306"><span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**\_propriété de stratégie d’interface utilisateur NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-306"><span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**NCRYPT\_UI\_POLICY\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-307">L "stratégie d’interface utilisateur"</span><span class="sxs-lookup"><span data-stu-id="9dedc-307">L"UI Policy"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-308">S’il est utilisé avec la fonction [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) ou [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) , il s’agit d’un pointeur vers une structure de [**stratégie d' \_ interface \_ utilisateur NCRYPT**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) qui contient la stratégie d’interface utilisateur de clé forte pour la clé.</span><span class="sxs-lookup"><span data-stu-id="9dedc-308">If used with the [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) or [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function, this is a pointer to an [**NCRYPT\_UI\_POLICY**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) structure that contains the strong key user interface policy for the key.</span></span> <span data-ttu-id="9dedc-309">Cette propriété s’applique uniquement aux clés persistantes.</span><span class="sxs-lookup"><span data-stu-id="9dedc-309">This property only applies to persistent keys.</span></span> <span data-ttu-id="9dedc-310">Cette propriété ne peut être définie que lorsque la clé est générée.</span><span class="sxs-lookup"><span data-stu-id="9dedc-310">This property can only be set when the key is being generated.</span></span> <span data-ttu-id="9dedc-311">Une fois que la fonction [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) a été appelée pour cette clé, cette propriété devient en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9dedc-311">Once the [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) function has been called for this key, this property becomes read-only.</span></span>

<span data-ttu-id="9dedc-312">Un fournisseur de stockage de clés peut recevoir ce paramètre par le biais d’une fonction de rappel [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) .</span><span class="sxs-lookup"><span data-stu-id="9dedc-312">A key storage provider can receive this parameter through an [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) callback function.</span></span> <span data-ttu-id="9dedc-313">La valeur du paramètre est une \_ \_ structure d’objet blob de stratégie d’interface utilisateur NCRYPT \_ qui contient les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="9dedc-313">The parameter value is an NCRYPT\_UI\_POLICY\_BLOB structure that contains the same information.</span></span> <span data-ttu-id="9dedc-314">De même, lorsqu’une application envoie une requête via NCryptSetPropertyFn au fournisseur pour retourner cette propriété, le fournisseur est supposé retourner une \_ \_ structure d’objet blob de stratégie d’interface utilisateur NCRYPT \_ .</span><span class="sxs-lookup"><span data-stu-id="9dedc-314">Similarly, when an application makes a request through NCryptSetPropertyFn to the provider to return this property, the provider is expected to return an NCRYPT\_UI\_POLICY\_BLOB structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-315"><span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**\_propriété de \_ nom \_ unique NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="9dedc-315"><span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**NCRYPT\_UNIQUE\_NAME\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-316">L "nom unique"</span><span class="sxs-lookup"><span data-stu-id="9dedc-316">L"Unique Name"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-317">Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le nom unique de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9dedc-317">A pointer to a null-terminated Unicode string that contains the unique name of the object.</span></span> <span data-ttu-id="9dedc-318">Il s’agit d’un autre nom qui peut être utilisé lors de l’accès à la clé.</span><span class="sxs-lookup"><span data-stu-id="9dedc-318">This is an alternate name that can be used when accessing the key.</span></span> <span data-ttu-id="9dedc-319">Cette propriété est utilisée lorsqu’il est supposé que le nom de clé initialement passé à [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) n’est pas suffisamment unique pour identifier de manière fiable la clé persistante.</span><span class="sxs-lookup"><span data-stu-id="9dedc-319">This property is used when it is thought that the key name originally passed to [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) is not unique enough to reliably identify the persisted key.</span></span> <span data-ttu-id="9dedc-320">Le fournisseur de stockage de clés Microsoft renverra le nom de fichier de la clé en tant que propriété.</span><span class="sxs-lookup"><span data-stu-id="9dedc-320">The Microsoft key storage provider will return the file name of the key as this property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-321"><span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**\_propriété de \_ contexte d’utilisation NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-321"><span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT\_USE\_CONTEXT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-322">L "utiliser le contexte"</span><span class="sxs-lookup"><span data-stu-id="9dedc-322">L"Use Context"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-323">Pointeur vers une chaîne Unicode terminée par le caractère null qui décrit le contexte de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9dedc-323">A pointer to a null-terminated Unicode string that describes the context of the operation.</span></span> <span data-ttu-id="9dedc-324">Cette propriété n’est pas persistante et peut être définie soit sur un fournisseur, soit sur une clé.</span><span class="sxs-lookup"><span data-stu-id="9dedc-324">This property is not persistent and can be set on either a provider or a key.</span></span> <span data-ttu-id="9dedc-325">Une clé n’a pas accès à la propriété de **\_ propriété de \_ contexte \_ NCRYPT use** du fournisseur, car la propriété est spécifique uniquement au handle pour lequel elle est définie.</span><span class="sxs-lookup"><span data-stu-id="9dedc-325">A key does not have access to the **NCRYPT\_USE\_CONTEXT\_PROPERTY** property of the provider because the property is specific only to the handle it is set for.</span></span>

<span data-ttu-id="9dedc-326">Un fournisseur de stockage de clés qui doit inviter l’utilisateur lors d’un appel à [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (par exemple, «insérez votre carte à puce dans le lecteur) est un exemple dans lequel cette propriété serait utilisée dans le contexte d’un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9dedc-326">An example where this property would be used in the context of a provider is a key storage provider that needs to prompt the user during a call to [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (for example, "Insert your smart card in the reader.").</span></span> <span data-ttu-id="9dedc-327">Étant donné que le handle de clé n’est pas disponible tant que **NCryptOpenKey** n’a pas retourné la valeur, l’application doit définir cette propriété sur le handle du fournisseur avant d’appeler **NCryptOpenKey**.</span><span class="sxs-lookup"><span data-stu-id="9dedc-327">Because the key handle is not available until after **NCryptOpenKey** returns, the application should set this property on the provider handle prior to calling **NCryptOpenKey**.</span></span>

<span data-ttu-id="9dedc-328">Voici un exemple dans lequel cette propriété serait utilisée dans le contexte d’un handle de clé. il s’agit d’un fournisseur de stockage de clés qui doit inviter l’utilisateur pendant une opération à l’aide de la clé (par exemple, « cette application a besoin d’utiliser cette clé pour signer un document. »).</span><span class="sxs-lookup"><span data-stu-id="9dedc-328">An example where this property would be used in the context of a key handle is a key storage provider that needs to prompt the user during an operation using the key (for example, "This application needs to use this key to sign a document.").</span></span> <span data-ttu-id="9dedc-329">Le fournisseur peut ensuite relayer ces informations de contexte à l’utilisateur dans n’importe quelle interface utilisateur affichée pendant l’opération.</span><span class="sxs-lookup"><span data-stu-id="9dedc-329">The provider could then relay this context information to the user in any user interface shown during the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-330"><span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**\_propriété NCRYPT use \_ Count \_ enabled \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-330"><span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**NCRYPT\_USE\_COUNT\_ENABLED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-331">L "nombre d’utilisations activées</span><span class="sxs-lookup"><span data-stu-id="9dedc-331">L"Enabled Use Count"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-332">Indique si le fournisseur prend en charge le comptage de l’utilisation des clés.</span><span class="sxs-lookup"><span data-stu-id="9dedc-332">Indicates whether the provider supports usage counting for keys.</span></span> <span data-ttu-id="9dedc-333">Cette propriété est une **valeur DWORD** qui contient 1 si le fournisseur prend en charge le comptage de l’utilisation des clés.</span><span class="sxs-lookup"><span data-stu-id="9dedc-333">This property is a **DWORD** that contains 1 if the provider supports usage counting for keys.</span></span> <span data-ttu-id="9dedc-334">Si cette propriété contient une autre valeur, ou si la fonction [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) retourne **NPD \_ non \_ pris en charge**, le fournisseur ne prend pas en charge le comptage de l’utilisation des clés.</span><span class="sxs-lookup"><span data-stu-id="9dedc-334">If this property contains any other value, or if the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function returns **NTE\_NOT\_SUPPORTED**, then the provider does not support usage counting for keys.</span></span> <span data-ttu-id="9dedc-335">Cette propriété s’applique uniquement aux fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="9dedc-335">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-336"><span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**\_propriété du \_ nombre d’utilisations de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-336"><span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**NCRYPT\_USE\_COUNT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-337">L "nombre d’utilisations"</span><span class="sxs-lookup"><span data-stu-id="9dedc-337">L"Use Count"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-338">Variable [**de \_ type entier ULARGE**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) qui contient le nombre d’opérations effectuées par la [*clé privée*](/windows/desktop/SecGloss/p-gly) spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9dedc-338">A [**ULARGE\_INTEGER**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) variable that contains the number of operations that the specified [*private key*](/windows/desktop/SecGloss/p-gly) has performed.</span></span> <span data-ttu-id="9dedc-339">Cette propriété est facultative et peut ne pas être prise en charge par tous les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="9dedc-339">This property is optional and may not be supported by all providers.</span></span> <span data-ttu-id="9dedc-340">Les fournisseurs qui prennent en charge cette propriété sur les clés doivent également prendre en charge la propriété de **\_ propriété NCRYPT use \_ Count \_ enabled \_** sur le descripteur du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9dedc-340">Providers that support this property on keys should also support the **NCRYPT\_USE\_COUNT\_ENABLED\_PROPERTY** property on the provider handle.</span></span> <span data-ttu-id="9dedc-341">Le fournisseur de stockage de clés Microsoft ne prend pas en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="9dedc-341">The Microsoft key storage provider does not support this property.</span></span> <span data-ttu-id="9dedc-342">Cette propriété s’applique uniquement aux clés persistantes.</span><span class="sxs-lookup"><span data-stu-id="9dedc-342">This property only applies to persistent keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-343"><span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**\_ \_ propriété CERTSTORE de l’utilisateur NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-343"><span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**NCRYPT\_USER\_CERTSTORE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-344">L « SmartCardUserCertStore »</span><span class="sxs-lookup"><span data-stu-id="9dedc-344">L"SmartCardUserCertStore"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-345">**HCERTSTORE** qui représente le magasin de certificats utilisateur de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="9dedc-345">An **HCERTSTORE** that represents the smart card user certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-346"><span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**\_propriété de version NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-346"><span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**NCRYPT\_VERSION\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-347">L "version"</span><span class="sxs-lookup"><span data-stu-id="9dedc-347">L"Version"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-348">**Valeur DWORD** qui contient la version du logiciel du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9dedc-348">A **DWORD** that contains the software version of the provider.</span></span> <span data-ttu-id="9dedc-349">Le mot de poids fort contient la version principale et le mot de poids faible contient la version mineure.</span><span class="sxs-lookup"><span data-stu-id="9dedc-349">The high word contains the major version and the low word contains the minor version.</span></span> <span data-ttu-id="9dedc-350">Par exemple, 0x00030033 = 3,51.</span><span class="sxs-lookup"><span data-stu-id="9dedc-350">For example, 0x00030033 = 3.51.</span></span> <span data-ttu-id="9dedc-351">Cette propriété s’applique uniquement aux fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="9dedc-351">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9dedc-352"><span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**\_propriété du \_ handle de fenêtre NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="9dedc-352"><span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**NCRYPT\_WINDOW\_HANDLE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dedc-353">L "handle HWND"</span><span class="sxs-lookup"><span data-stu-id="9dedc-353">L"HWND Handle"</span></span>
</dt> <dt>



<span data-ttu-id="9dedc-354">Pointeur vers le handle de fenêtre (**HWND**) à utiliser comme parent de toute interface utilisateur affichée.</span><span class="sxs-lookup"><span data-stu-id="9dedc-354">A pointer to the window handle (**HWND**) to be used as the parent of any user interface that is displayed.</span></span>

<span data-ttu-id="9dedc-355">Comme un comportement indésirable peut se produire lorsqu’une interface utilisateur est affichée à l’aide d’un handle de fenêtre **null** pour le parent, nous vous recommandons vivement qu’un fournisseur de stockage de clés n’affiche pas d’interface utilisateur, sauf si cette propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="9dedc-355">Because undesirable behavior can happen when a user interface is shown by using a **NULL** window handle for the parent, we strongly recommend that a key storage provider not display a user interface unless this property is set.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="9dedc-356">Les valeurs suivantes sont utilisées pour définir les limites des données de propriété.</span><span class="sxs-lookup"><span data-stu-id="9dedc-356">The following values are used to define limits of property data.</span></span>



| <span data-ttu-id="9dedc-357">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="9dedc-357">Constant/value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="9dedc-358">Description</span><span class="sxs-lookup"><span data-stu-id="9dedc-358">Description</span></span>                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <span data-ttu-id="9dedc-359"><dt>**NCRYPT \_ Nombre maximal de \_ \_ données de propriété**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9dedc-359"><dt>**NCRYPT\_MAX\_PROPERTY\_DATA**</dt> <dt>0x100000</dt></span></span> </dl> | <span data-ttu-id="9dedc-360">Spécifie la taille maximale, en octets, d’une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="9dedc-360">Specifies the maximum size of a property value, in bytes.</span></span><br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <span data-ttu-id="9dedc-361"><dt>**NCRYPT \_ \_ \_ Nom de propriété max**</dt> <dt>64</dt></span><span class="sxs-lookup"><span data-stu-id="9dedc-361"><dt>**NCRYPT\_MAX\_PROPERTY\_NAME**</dt> <dt>64</dt></span></span> </dl>       | <span data-ttu-id="9dedc-362">Spécifie la taille maximale d’un nom de propriété, en caractères.</span><span class="sxs-lookup"><span data-stu-id="9dedc-362">Specifies the maximum size of a property name, in characters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9dedc-363">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9dedc-363">Requirements</span></span>



| <span data-ttu-id="9dedc-364">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9dedc-364">Requirement</span></span> | <span data-ttu-id="9dedc-365">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dedc-365">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9dedc-366">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9dedc-366">Minimum supported client</span></span><br/> | <span data-ttu-id="9dedc-367">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9dedc-367">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9dedc-368">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9dedc-368">Minimum supported server</span></span><br/> | <span data-ttu-id="9dedc-369">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9dedc-369">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9dedc-370">En-tête</span><span class="sxs-lookup"><span data-stu-id="9dedc-370">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dedc-371"><dt>Ncrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dedc-371"><dt>Ncrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dedc-372">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dedc-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dedc-373">**NCryptGetProperty**</span><span class="sxs-lookup"><span data-stu-id="9dedc-373">**NCryptGetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[<span data-ttu-id="9dedc-374">**NCryptSetProperty**</span><span class="sxs-lookup"><span data-stu-id="9dedc-374">**NCryptSetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 

