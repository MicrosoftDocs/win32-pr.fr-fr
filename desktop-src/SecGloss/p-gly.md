---
description: Contient les définitions des termes de sécurité qui commencent par la lettre P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a
title: P (Glossaire de la sécurité)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd5b580295c35bc021ade53d3cb922ce8fe13d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866630"
---
# <a name="p-security-glossary"></a><span data-ttu-id="61c55-103">P (Glossaire de la sécurité)</span><span class="sxs-lookup"><span data-stu-id="61c55-103">P (Security Glossary)</span></span>

<span data-ttu-id="61c55-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="61c55-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="61c55-105"><span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**remplissage**</span><span class="sxs-lookup"><span data-stu-id="61c55-105"><span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**padding**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-106">Chaîne, généralement ajoutée quand le dernier bloc de texte en clair est court.</span><span class="sxs-lookup"><span data-stu-id="61c55-106">A string, typically added when the last plaintext block is short.</span></span> <span data-ttu-id="61c55-107">Par exemple, si la longueur de bloc est de 64 bits et que le dernier bloc contient uniquement 40 bits, 24 bits de remplissage doivent être ajoutés au dernier bloc.</span><span class="sxs-lookup"><span data-stu-id="61c55-107">For example, if the block length is 64 bits and the last block contains only 40 bits, then 24 bits of padding must be added to the last block.</span></span> <span data-ttu-id="61c55-108">La chaîne de remplissage peut contenir des zéros, des zéros et des zéros, ou un autre modèle.</span><span class="sxs-lookup"><span data-stu-id="61c55-108">The padding string may contain zeros, alternating zeros and ones, or some other pattern.</span></span> <span data-ttu-id="61c55-109">Les applications qui utilisent [*CryptoAPI*](c-gly.md) n’ont pas besoin d’ajouter un remplissage à leur texte en clair avant d’être chiffrées, ni de les supprimer après le déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="61c55-109">Applications that use [*CryptoAPI*](c-gly.md) need not add padding to their plaintext before it is encrypted, nor do they have to remove it after decrypting.</span></span> <span data-ttu-id="61c55-110">Tout est géré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="61c55-110">This is all handled automatically.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-111"><span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**filtre de mot de passe**</span><span class="sxs-lookup"><span data-stu-id="61c55-111"><span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**password filter**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-112">DLL qui fournit une mise en œuvre de la stratégie de mot de passe et une notification de modification.</span><span class="sxs-lookup"><span data-stu-id="61c55-112">A DLL that provides password policy enforcement and change notification.</span></span> <span data-ttu-id="61c55-113">Les fonctions implémentées par les filtres de mot de passe sont appelées par l' [*autorité de sécurité locale*](l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="61c55-113">The functions implemented by password filters are called by the [*Local Security Authority*](l-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="61c55-114"><span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**stockage persistant**</span><span class="sxs-lookup"><span data-stu-id="61c55-114"><span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**persistent storage**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-115">Tout support de stockage qui reste intact lorsque la puissance est déconnectée.</span><span class="sxs-lookup"><span data-stu-id="61c55-115">Any storage medium that remains intact when the power to it is disconnected.</span></span> <span data-ttu-id="61c55-116">De nombreuses bases de données du [*magasin de certificats*](c-gly.md) sont des formes de stockage persistant.</span><span class="sxs-lookup"><span data-stu-id="61c55-116">Many [*certificate store*](c-gly.md) databases are forms of persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-117"><span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS#12**</span><span class="sxs-lookup"><span data-stu-id="61c55-117"><span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-118">Consultez *normes de cryptographie à clé publique*.</span><span class="sxs-lookup"><span data-stu-id="61c55-118">See *Public Key Cryptography Standards*.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-119"><span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \# 1**</span><span class="sxs-lookup"><span data-stu-id="61c55-119"><span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \#1**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-120">Normes recommandées pour l’implémentation du chiffrement à clé publique basée sur l’algorithme RSA, tel que défini dans la [norme RFC 3447](https://tools.ietf.org/html/rfc3447).</span><span class="sxs-lookup"><span data-stu-id="61c55-120">The recommended standards for the implementation of public-key cryptography based on the RSA algorithm as defined in [RFC 3447](https://tools.ietf.org/html/rfc3447).</span></span>

</dd> <dt>

<span data-ttu-id="61c55-121"><span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \# 12**</span><span class="sxs-lookup"><span data-stu-id="61c55-121"><span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \#12**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-122">Norme, développée et gérée par RSA Data Security, Inc. Cette norme de syntaxe spécifie un format portable pour le stockage ou le transport des clés privées, des certificats et des secrets divers d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="61c55-122">The Personal Information Exchange Syntax Standard, developed and maintained by RSA Data Security, Inc. This syntax standard specifies a portable format for storing or transporting a user's private keys, certificates, and miscellaneous secrets.</span></span>

<span data-ttu-id="61c55-123">Voir également les *normes de chiffrement* des [*certificats*](c-gly.md) et des clés publiques.</span><span class="sxs-lookup"><span data-stu-id="61c55-123">See also [*certificate*](c-gly.md) and *Public Key Cryptography Standards*.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-124"><span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**\#Données signées PKCS 7**</span><span class="sxs-lookup"><span data-stu-id="61c55-124"><span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**PKCS \#7 Signed Data**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-125">Objet de données signé avec la norme publique de chiffrement à clé publique \# 7 (PKCS \# 7) et qui encapsule les informations utilisées pour signer un fichier.</span><span class="sxs-lookup"><span data-stu-id="61c55-125">A data object that is signed with the Public Key Cryptography Standard \#7 (PKCS \#7) and that encapsulates the information used to sign a file.</span></span> <span data-ttu-id="61c55-126">En règle générale, il comprend le certificat du signataire et le [*certificat racine*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="61c55-126">Typically, it includes the signer's certificate and the [*root certificate*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="61c55-127"><span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \# 7**</span><span class="sxs-lookup"><span data-stu-id="61c55-127"><span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \#7**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-128">Norme de syntaxe de message de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="61c55-128">The Cryptographic Message Syntax Standard.</span></span> <span data-ttu-id="61c55-129">Syntaxe générale des données auxquelles le chiffrement peut être appliqué, telles que les signatures numériques et le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="61c55-129">A general syntax for data to which cryptography may be applied, such as digital signatures and encryption.</span></span> <span data-ttu-id="61c55-130">Il fournit également une syntaxe pour diffuser des certificats ou des listes de révocation de certificats et d’autres attributs de message, tels que des horodatages, au message.</span><span class="sxs-lookup"><span data-stu-id="61c55-130">It also provides a syntax for disseminating certificates or certificate revocation lists and other message attributes, such as time stamps, to the message.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-131"><span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**Encodage ASN de PKCS \_ 7 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="61c55-131"><span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**PKCS\_7\_ASN\_ENCODING**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-132">[*Type d’encodage de message*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="61c55-132">A [*message encoding type*](m-gly.md).</span></span> <span data-ttu-id="61c55-133">Les types d’encodage de message sont stockés dans le mot de poids fort d’une valeur **DWORD** (la valeur est : 0x00010000).</span><span class="sxs-lookup"><span data-stu-id="61c55-133">Message encoding types are stored in the high-order word of a **DWORD** (value is: 0x00010000).</span></span>

</dd> <dt>

<span data-ttu-id="61c55-134"><span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**en**</span><span class="sxs-lookup"><span data-stu-id="61c55-134"><span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**plaintext**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-135">Message non chiffré.</span><span class="sxs-lookup"><span data-stu-id="61c55-135">A message that is not encrypted.</span></span> <span data-ttu-id="61c55-136">Les messages en texte brut sont quelquefois connus sous le nom de messages en texte clair.</span><span class="sxs-lookup"><span data-stu-id="61c55-136">Plaintext messages are sometimes referred to as cleartext messages.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-137"><span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Image PE (Portable Executable)**</span><span class="sxs-lookup"><span data-stu-id="61c55-137"><span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Portable Executable (PE) Image**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-138">Format d’exécutable Windows standard.</span><span class="sxs-lookup"><span data-stu-id="61c55-138">The standard Windows executable format.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-139"><span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**</span><span class="sxs-lookup"><span data-stu-id="61c55-139"><span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-140">Consultez *fonction Pseudo-aléatoire*.</span><span class="sxs-lookup"><span data-stu-id="61c55-140">See *Pseudo-Random Function*.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-141"><span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**informations d’identification principales**</span><span class="sxs-lookup"><span data-stu-id="61c55-141"><span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**primary credentials**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-142">Le \_ package d’authentification MsV1 0 définit une valeur de chaîne de clé d’informations d’identification primaire : la chaîne d’informations d’identification principales contient les informations d’identification fournies lors de l’ouverture de session initiale.</span><span class="sxs-lookup"><span data-stu-id="61c55-142">The MsV1\_0 authentication package defines a primary credential key string value: The primary credentials string holds the credentials provided at initial logon time.</span></span> <span data-ttu-id="61c55-143">Il comprend le nom d’utilisateur et les formes qui respectent la casse et qui ne respectent pas la casse du mot de passe de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="61c55-143">It includes the user name and both case-sensitive and case-insensitive forms of the user's password.</span></span>

<span data-ttu-id="61c55-144">Voir aussi [*informations d’identification supplémentaires*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="61c55-144">See also [*supplemental credentials*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="61c55-145"><span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**fournisseur de services principal**</span><span class="sxs-lookup"><span data-stu-id="61c55-145"><span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**primary service provider**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-146">Fournisseur de services qui fournit les interfaces de contrôle à la carte.</span><span class="sxs-lookup"><span data-stu-id="61c55-146">The service provider that supplies the control interfaces to the card.</span></span> <span data-ttu-id="61c55-147">Chaque carte à puce peut inscrire son fournisseur de services principal dans la base de données des cartes à puce.</span><span class="sxs-lookup"><span data-stu-id="61c55-147">Each smart card can register its primary service provider in the smart card database.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-148"><span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**jeton principal**</span><span class="sxs-lookup"><span data-stu-id="61c55-148"><span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**primary token**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-149">Jeton d’accès qui est généralement créé uniquement par le noyau Windows.</span><span class="sxs-lookup"><span data-stu-id="61c55-149">An access token that is typically created only by the Windows kernel.</span></span> <span data-ttu-id="61c55-150">Il peut être assigné à un processus pour représenter les informations de sécurité par défaut pour ce processus.</span><span class="sxs-lookup"><span data-stu-id="61c55-150">It may be assigned to a process to represent the default security information for that process.</span></span>

<span data-ttu-id="61c55-151">Voir aussi jeton d' [*accès*](a-gly.md) et jeton d' [*emprunt d’identité*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="61c55-151">See also [*access token*](a-gly.md) and [*impersonation token*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="61c55-152"><span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**Directeur**</span><span class="sxs-lookup"><span data-stu-id="61c55-152"><span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**principal**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-153">Consultez [*principal de sécurité*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="61c55-153">See [*security principal*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="61c55-154"><span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**nominative**</span><span class="sxs-lookup"><span data-stu-id="61c55-154"><span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**privacy**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-155">Condition qui est isolée de la vue ou du secret.</span><span class="sxs-lookup"><span data-stu-id="61c55-155">The condition of being isolated from view or secret.</span></span> <span data-ttu-id="61c55-156">En ce qui concerne les messages, les messages privés sont des messages chiffrés dont le texte est masqué.</span><span class="sxs-lookup"><span data-stu-id="61c55-156">With respect to messages, private messages are encrypted messages whose text is hidden from view.</span></span> <span data-ttu-id="61c55-157">En ce qui concerne les clés, une clé privée est une clé secrète masquée des autres.</span><span class="sxs-lookup"><span data-stu-id="61c55-157">With respect to keys, a private key is a secret key concealed from others.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-158"><span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**clé privée**</span><span class="sxs-lookup"><span data-stu-id="61c55-158"><span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**private key**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-159">Moitié secrète d’une paire de clés utilisée dans un algorithme de clé publique.</span><span class="sxs-lookup"><span data-stu-id="61c55-159">The secret half of a key pair used in a public key algorithm.</span></span> <span data-ttu-id="61c55-160">Les clés privées sont utilisées en général pour chiffrer une clé de session symétrique, signer numériquement un message ou déchiffrer un message qui a été chiffré avec la clé publique correspondante.</span><span class="sxs-lookup"><span data-stu-id="61c55-160">Private keys are typically used to encrypt a symmetric session key, digitally sign a message, or decrypt a message that has been encrypted with the corresponding public key.</span></span>

<span data-ttu-id="61c55-161">Voir aussi *clé publique*.</span><span class="sxs-lookup"><span data-stu-id="61c55-161">See also *public key*.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-162"><span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**BLOB de clé privée**</span><span class="sxs-lookup"><span data-stu-id="61c55-162"><span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**private key BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-163">Objet BLOB de clé qui contient une paire de clés publique/privée complète.</span><span class="sxs-lookup"><span data-stu-id="61c55-163">A key BLOB that contains a complete public/private key pair.</span></span> <span data-ttu-id="61c55-164">Les objets BLOB de clé privée sont utilisés par les programmes d’administration pour transporter les paires de clés.</span><span class="sxs-lookup"><span data-stu-id="61c55-164">Private key BLOBs are used by administrative programs to transport key pairs.</span></span> <span data-ttu-id="61c55-165">Comme la partie clé privée de la paire de clés est extrêmement confidentielle, ces objets BLOB sont généralement gardés chiffrés à l’aide d’un chiffrement symétrique.</span><span class="sxs-lookup"><span data-stu-id="61c55-165">As the private key portion of the key pair is extremely confidential, these BLOBs are typically kept encrypted with a symmetric cipher.</span></span> <span data-ttu-id="61c55-166">Ces objets BLOB de clé peuvent également être utilisés par les applications avancées où les paires de clés sont stockées au sein de l’application, plutôt que de s’appuyer sur le mécanisme de stockage du CSP.</span><span class="sxs-lookup"><span data-stu-id="61c55-166">These key BLOBs can also be used by advanced applications where the key pairs are stored within the application, rather than relying on the CSP's storage mechanism.</span></span> <span data-ttu-id="61c55-167">Un objet BLOB de clé est créé en appelant la fonction **CryptExportKey** .</span><span class="sxs-lookup"><span data-stu-id="61c55-167">A key BLOB is created by calling the **CryptExportKey** function.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-168"><span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**limités**</span><span class="sxs-lookup"><span data-stu-id="61c55-168"><span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**privilege**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-169">Droit d'un utilisateur à exécuter différentes opérations relatives au système, telles que l'arrêt du système, le chargement de pilotes de périphériques, ou la modification de l'heure système.</span><span class="sxs-lookup"><span data-stu-id="61c55-169">The right of a user to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span> <span data-ttu-id="61c55-170">Le jeton d’accès d’un utilisateur contient une liste des privilèges détenus par l’utilisateur ou par les groupes de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="61c55-170">A user's access token contains a list of the privileges held by either the user or the user's groups.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-171"><span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**traiter**</span><span class="sxs-lookup"><span data-stu-id="61c55-171"><span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**process**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-172">Contexte de sécurité dans lequel une application s'exécute.</span><span class="sxs-lookup"><span data-stu-id="61c55-172">The security context under which an application runs.</span></span> <span data-ttu-id="61c55-173">En général, le contexte de sécurité est associé à un utilisateur, donc toutes les applications qui s'exécutent dans un processus donné récupèrent les autorisations et les privilèges de l'utilisateur à qui elles appartiennent.</span><span class="sxs-lookup"><span data-stu-id="61c55-173">Typically, the security context is associated with a user, so all applications running under a given process take on the permissions and privileges of the owning user.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-174"><span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**DSS PROVen \_**</span><span class="sxs-lookup"><span data-stu-id="61c55-174"><span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**PROV\_DSS**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-175">Consultez *\_ type de fournisseur DSS Proven*.</span><span class="sxs-lookup"><span data-stu-id="61c55-175">See *PROV\_DSS provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-176"><span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**Type de fournisseur PROVen \_ DSS**</span><span class="sxs-lookup"><span data-stu-id="61c55-176"><span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**PROV\_DSS Provider Type**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-177">Type de fournisseur prédéfini qui prend uniquement en charge les signatures numériques et les hachages.</span><span class="sxs-lookup"><span data-stu-id="61c55-177">Predefined provider type that only supports digital signatures and hashes.</span></span> <span data-ttu-id="61c55-178">Il spécifie l’algorithme de signature DSA et les algorithmes de hachage MD5 et SHA-1.</span><span class="sxs-lookup"><span data-stu-id="61c55-178">It specifies the DSA signature algorithm, and the MD5 and SHA-1 hashing algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-179"><span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**PROVen \_ DSS \_**</span><span class="sxs-lookup"><span data-stu-id="61c55-179"><span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**PROV\_DSS\_DH**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-180">Consultez *le \_ \_ type de fournisseur Proven DSS*.</span><span class="sxs-lookup"><span data-stu-id="61c55-180">See *PROV\_DSS\_DH provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-181"><span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**\_Type de fournisseur prouvé DSS- \_ DH**</span><span class="sxs-lookup"><span data-stu-id="61c55-181"><span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**PROV\_DSS\_DH provider type**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-182">Type de fournisseur prédéfini qui fournit l’échange de clés, la signature numérique et les algorithmes de hachage.</span><span class="sxs-lookup"><span data-stu-id="61c55-182">Predefined provider type that provides key exchange, digital signature, and hashing algorithms.</span></span> <span data-ttu-id="61c55-183">Elle est similaire au type de \_ fournisseur DSS Proven.</span><span class="sxs-lookup"><span data-stu-id="61c55-183">It is similar to the PROV\_DSS provider type.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-184"><span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**\_Fortezza-Fortezza**</span><span class="sxs-lookup"><span data-stu-id="61c55-184"><span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**PROV\_FORTEZZA**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-185">Consultez *\_ type de fournisseur Fortezza*.</span><span class="sxs-lookup"><span data-stu-id="61c55-185">See *PROV\_FORTEZZA provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-186"><span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**Type de fournisseur Fortezza de la preuve \_**</span><span class="sxs-lookup"><span data-stu-id="61c55-186"><span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**PROV\_FORTEZZA provider type**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-187">Type de fournisseur prédéfini qui fournit l’échange de clés, la signature numérique, le chiffrement et les algorithmes de hachage.</span><span class="sxs-lookup"><span data-stu-id="61c55-187">Predefined provider type that provides key exchange, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="61c55-188">Les protocoles et algorithmes de chiffrement spécifiés par ce type de fournisseur sont détenus par le NIST (National Institute of Standards and Technology).</span><span class="sxs-lookup"><span data-stu-id="61c55-188">The cryptographic protocols and algorithms specified by this provider type are owned by the National Institute of Standards and Technology (NIST).</span></span>

</dd> <dt>

<span data-ttu-id="61c55-189"><span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROUVER \_ MS \_ Exchange**</span><span class="sxs-lookup"><span data-stu-id="61c55-189"><span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROV\_MS\_EXCHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-190">Consultez *\_ type de \_ fournisseur MS Exchange Prov*.</span><span class="sxs-lookup"><span data-stu-id="61c55-190">See *PROV\_MS\_EXCHANGE provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-191"><span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**\_Type de \_ fournisseur MS Exchange Prov.**</span><span class="sxs-lookup"><span data-stu-id="61c55-191"><span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**PROV\_MS\_EXCHANGE provider type**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-192">Type de fournisseur prédéfini conçu pour les besoins de Microsoft Exchange, ainsi que d’autres applications compatibles avec Microsoft Mail.</span><span class="sxs-lookup"><span data-stu-id="61c55-192">Predefined provider type designed for the needs of Microsoft Exchange, as well as other applications that are compatible with Microsoft Mail.</span></span> <span data-ttu-id="61c55-193">Il fournit l’échange de clés, la signature numérique, le chiffrement et les algorithmes de hachage.</span><span class="sxs-lookup"><span data-stu-id="61c55-193">It provides key exchange, digital signature, encryption, and hashing algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-194"><span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROUVER \_ RSA \_ Full**</span><span class="sxs-lookup"><span data-stu-id="61c55-194"><span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROV\_RSA\_FULL**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-195">Consultez la page *prouver le \_ type de \_ fournisseur complet RSA*.</span><span class="sxs-lookup"><span data-stu-id="61c55-195">See *PROV\_RSA\_FULL provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-196"><span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**\_Type de \_ fournisseur complet RSA Prov.**</span><span class="sxs-lookup"><span data-stu-id="61c55-196"><span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**PROV\_RSA\_FULL provider type**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-197">Type de fournisseur prédéfini défini par Microsoft et RSA Data Security, Inc. Ce type de fournisseur à usage général fournit l’échange de clés, la signature numérique, le chiffrement et les algorithmes de hachage.</span><span class="sxs-lookup"><span data-stu-id="61c55-197">Predefined provider type defined by Microsoft and RSA Data Security, Inc. This general purpose provider type provides key exchange, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="61c55-198">L’échange de clés, la signature numérique et les algorithmes de chiffrement sont basés sur le chiffrement à clé publique RSA.</span><span class="sxs-lookup"><span data-stu-id="61c55-198">The key exchange, digital signature, and encryption algorithms are based on RSA public key cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-199"><span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROUVER \_ RSA \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="61c55-199"><span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROV\_RSA\_SIG**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-200">Consultez la page *prouver le \_ type de \_ fournisseur RSA SIG*.</span><span class="sxs-lookup"><span data-stu-id="61c55-200">See *PROV\_RSA\_SIG provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-201"><span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**\_Type de \_ fournisseur prouver RSA SIG**</span><span class="sxs-lookup"><span data-stu-id="61c55-201"><span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**PROV\_RSA\_SIG provider type**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-202">Type de fournisseur prédéfini défini par Microsoft et RSA Data Security.</span><span class="sxs-lookup"><span data-stu-id="61c55-202">Predefined provider type defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="61c55-203">Ce type de fournisseur est un sous-ensemble de la preuve \_ \_ complète RSA qui fournit uniquement des algorithmes de hachage et de signature numérique.</span><span class="sxs-lookup"><span data-stu-id="61c55-203">This provider type is a subset of PROV\_RSA\_FULL that provides only digital signature and hashing algorithms.</span></span> <span data-ttu-id="61c55-204">L’algorithme de signature numérique est un algorithme de clé publique RSA.</span><span class="sxs-lookup"><span data-stu-id="61c55-204">The digital signature algorithm is an RSA public key algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-205"><span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**SSL PROV. \_**</span><span class="sxs-lookup"><span data-stu-id="61c55-205"><span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**PROV\_SSL**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-206">Consultez *\_ type de fournisseur SSL Prov*.</span><span class="sxs-lookup"><span data-stu-id="61c55-206">See *PROV\_SSL provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-207"><span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**\_Type de fournisseur de chiffrement SSL Prov**</span><span class="sxs-lookup"><span data-stu-id="61c55-207"><span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**PROV\_SSL provider type**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-208">Type de fournisseur prédéfini qui prend en charge le protocole SSL (Secure Sockets Layer) (SSL).</span><span class="sxs-lookup"><span data-stu-id="61c55-208">Predefined provider type that supports the Secure Sockets Layer (SSL) protocol.</span></span> <span data-ttu-id="61c55-209">Ce type fournit le chiffrement à clé, la signature numérique, le chiffrement et les algorithmes de hachage.</span><span class="sxs-lookup"><span data-stu-id="61c55-209">This type provides key encryption, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="61c55-210">Une spécification décrivant le protocole SSL est disponible auprès de Netscape Communications Corp.</span><span class="sxs-lookup"><span data-stu-id="61c55-210">A specification explaining SSL is available from Netscape Communications Corp.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-211"><span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**moteur**</span><span class="sxs-lookup"><span data-stu-id="61c55-211"><span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-212">Consultez [*fournisseur de services de chiffrement*](c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="61c55-212">See [*Cryptographic Service Provider*](c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="61c55-213"><span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**nom du fournisseur**</span><span class="sxs-lookup"><span data-stu-id="61c55-213"><span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**provider name**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-214">Nom utilisé pour identifier un CSP.</span><span class="sxs-lookup"><span data-stu-id="61c55-214">A name used to identify a CSP.</span></span> <span data-ttu-id="61c55-215">Par exemple, le fournisseur de services de chiffrement de base Microsoft version 1,0.</span><span class="sxs-lookup"><span data-stu-id="61c55-215">For example, the Microsoft Base Cryptographic Provider version 1.0.</span></span> <span data-ttu-id="61c55-216">Le nom du fournisseur est généralement utilisé lors de l’appel de la fonction **CryptAcquireContext** pour se connecter à un CSP.</span><span class="sxs-lookup"><span data-stu-id="61c55-216">The provider name is typically used when calling the **CryptAcquireContext** function to connect to a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-217"><span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**type de fournisseur**</span><span class="sxs-lookup"><span data-stu-id="61c55-217"><span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**provider type**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-218">Terme utilisé pour identifier un type de fournisseur de services de chiffrement (CSP).</span><span class="sxs-lookup"><span data-stu-id="61c55-218">A term used to identify a type of cryptographic service provider (CSP).</span></span> <span data-ttu-id="61c55-219">Les fournisseurs de services de chiffrement sont regroupés en différents types de fournisseurs qui représentent une famille spécifique de formats de données et de protocoles standard.</span><span class="sxs-lookup"><span data-stu-id="61c55-219">CSPs are grouped into different provider types that represent a specific families of standard data formats and protocols.</span></span> <span data-ttu-id="61c55-220">Contrairement au nom unique du fournisseur CSP, les types de fournisseurs ne sont pas uniques pour un CSP donné.</span><span class="sxs-lookup"><span data-stu-id="61c55-220">In contrast to a CSP's unique provider name, provider types are not unique for a given CSP.</span></span> <span data-ttu-id="61c55-221">Le type de fournisseur est généralement utilisé lors de l’appel de la fonction **CryptAcquireContext** pour se connecter à un CSP.</span><span class="sxs-lookup"><span data-stu-id="61c55-221">The provider type is typically used when calling the **CryptAcquireContext** function to connect to a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-222"><span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**fonction Pseudo-aléatoire**</span><span class="sxs-lookup"><span data-stu-id="61c55-222"><span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**pseudo-random function**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-223">PRF Fonction qui prend une clé, une étiquette et une valeur initiale comme entrée, puis produit une sortie de longueur arbitraire.</span><span class="sxs-lookup"><span data-stu-id="61c55-223">(PRF) A function that takes a key, label, and seed as input, then produces an output of arbitrary length.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-224"><span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**paire de clés publique/privée**</span><span class="sxs-lookup"><span data-stu-id="61c55-224"><span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**public/private key pair**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-225">Jeu de clés de chiffrement utilisé pour le chiffrement à clé publique.</span><span class="sxs-lookup"><span data-stu-id="61c55-225">A set of cryptographic keys used for public key cryptography.</span></span> <span data-ttu-id="61c55-226">Pour chaque utilisateur, un fournisseur de services Cloud gère généralement deux paires de clés publiques/privées : une paire de clés d’échange et une paire de clés de signature numérique.</span><span class="sxs-lookup"><span data-stu-id="61c55-226">For each user, a CSP usually maintains two public/private key pairs: an exchange key pair and a digital signature key pair.</span></span> <span data-ttu-id="61c55-227">Les deux paires de clés sont conservées d'une session à une autre.</span><span class="sxs-lookup"><span data-stu-id="61c55-227">Both key pairs are maintained from session to session.</span></span>

<span data-ttu-id="61c55-228">Consultez paire de clés et paire de [*clés de signature*](s-gly.md) [*Exchange*](e-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="61c55-228">See [*exchange key pair*](e-gly.md) and [*signature key pair*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="61c55-229"><span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**clé publique**</span><span class="sxs-lookup"><span data-stu-id="61c55-229"><span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**public key**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-230">Clé de chiffrement utilisée en général pour déchiffrer une clé de session ou une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="61c55-230">A cryptographic key typically used when decrypting a session key or a digital signature.</span></span> <span data-ttu-id="61c55-231">La clé publique peut également être utilisée pour chiffrer un message, ce qui garantit que seule la personne avec la clé privée correspondante peut déchiffrer le message.</span><span class="sxs-lookup"><span data-stu-id="61c55-231">The public key can also be used to encrypt a message, guaranteeing that only the person with the corresponding private key can decrypt the message.</span></span>

<span data-ttu-id="61c55-232">Voir aussi *clé privée*.</span><span class="sxs-lookup"><span data-stu-id="61c55-232">See also *private key*.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-233"><span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**algorithme de clé publique**</span><span class="sxs-lookup"><span data-stu-id="61c55-233"><span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**public key algorithm**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-234">Un chiffrement asymétrique qui utilise deux clés : une pour le chiffrement, la clé publique et l’autre pour le déchiffrement, la clé privée.</span><span class="sxs-lookup"><span data-stu-id="61c55-234">An asymmetric cipher that uses two keys, one for encryption, the public key, and the other for decryption, the private key.</span></span> <span data-ttu-id="61c55-235">Comme les noms de clé le présupposent, la clé publique utilisée pour encoder du texte brut peut être mise à la disposition de tout le monde.</span><span class="sxs-lookup"><span data-stu-id="61c55-235">As implied by the key names, the public key used to encode plaintext can be made available to anyone.</span></span> <span data-ttu-id="61c55-236">Toutefois, la clé privée doit rester secrète.</span><span class="sxs-lookup"><span data-stu-id="61c55-236">However, the private key must remain secret.</span></span> <span data-ttu-id="61c55-237">Seule la clé privée peut déchiffrer le texte chiffré.</span><span class="sxs-lookup"><span data-stu-id="61c55-237">Only the private key can decrypt the ciphertext.</span></span> <span data-ttu-id="61c55-238">L’algorithme de clé publique utilisé dans ce processus est lent (de l’ordre de 1 000 fois plus lentement que les algorithmes symétriques), et est généralement utilisé pour chiffrer les clés de session ou signer numériquement un message.</span><span class="sxs-lookup"><span data-stu-id="61c55-238">The public key algorithm used in this process is slow (on the order of 1,000 times slower than symmetric algorithms), and is typically used to encrypt session keys or digitally sign a message.</span></span>

<span data-ttu-id="61c55-239">Voir aussi *clé publique* et *clé privée*.</span><span class="sxs-lookup"><span data-stu-id="61c55-239">See also *public key* and *private key*.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-240"><span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**objet BLOB de clé publique**</span><span class="sxs-lookup"><span data-stu-id="61c55-240"><span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**public key BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-241">Objet BLOB utilisé pour stocker la partie clé publique d’une paire de clés publique/privée.</span><span class="sxs-lookup"><span data-stu-id="61c55-241">A BLOB used to store the public key portion of a public/private key pair.</span></span> <span data-ttu-id="61c55-242">Les objets BLOB de clé publique ne sont pas chiffrés, car la clé publique contenue dans n’est pas secrète.</span><span class="sxs-lookup"><span data-stu-id="61c55-242">Public key BLOBs are not encrypted as the public key contained within is not secret.</span></span> <span data-ttu-id="61c55-243">Un objet BLOB de clé publique est créé en appelant la fonction **CryptExportKey** .</span><span class="sxs-lookup"><span data-stu-id="61c55-243">A public key BLOB is created by calling the **CryptExportKey** function.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-244"><span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Normes de chiffrement à clé publique**</span><span class="sxs-lookup"><span data-stu-id="61c55-244"><span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Public Key Cryptography Standards**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-245">PKCS#12 Ensemble de normes syntaxiques pour le chiffrement à clé publique couvrant les fonctions de sécurité, y compris les méthodes pour la signature des données, l’échange de clés, la demande de certificats, le chiffrement et le déchiffrement à clé publique, ainsi que d’autres fonctions de sécurité.</span><span class="sxs-lookup"><span data-stu-id="61c55-245">(PKCS) A set of syntax standards for public key cryptography covering security functions, including methods for signing data, exchanging keys, requesting certificates, public key encryption and decryption, and other security functions.</span></span>

</dd> <dt>

<span data-ttu-id="61c55-246"><span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**chiffrement à clé publique**</span><span class="sxs-lookup"><span data-stu-id="61c55-246"><span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**public key encryption**</span></span>
</dt> <dd>

<span data-ttu-id="61c55-247">Chiffrement qui utilise une paire de clés, une clé pour chiffrer des données et une autre clé pour déchiffrer des données.</span><span class="sxs-lookup"><span data-stu-id="61c55-247">Encryption that uses a pair of keys, one key to encrypt data and the other key to decrypt data.</span></span> <span data-ttu-id="61c55-248">Par opposition, algorithmes de chiffrement symétrique qui utilisent la même clé à la fois pour le chiffrement et le déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="61c55-248">In contrast, symmetric encryption algorithms that use the same key for both encryption and decryption.</span></span> <span data-ttu-id="61c55-249">Dans la pratique, le chiffrement à clé publique est généralement utilisé pour protéger la clé de session utilisée par un algorithme de chiffrement symétrique.</span><span class="sxs-lookup"><span data-stu-id="61c55-249">In practice, public key cryptography is typically used to protect the session key used by a symmetric encryption algorithm.</span></span> <span data-ttu-id="61c55-250">Dans ce cas, la clé publique est utilisée pour chiffrer la clé de session, qui a ensuite été utilisée pour chiffrer des données, et la clé privée est utilisée pour le déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="61c55-250">In this case, the public key is used to encrypt the session key, which in turn was used to encrypt some data, and the private key is used for decryption.</span></span> <span data-ttu-id="61c55-251">En plus de protéger les clés de session, le chiffrement à clé publique peut également être utilisé pour signer un message numériquement (à l'aide de la clé privée) et valider la signature (à l'aide de la clé publique).</span><span class="sxs-lookup"><span data-stu-id="61c55-251">In addition to protecting session keys, public key cryptography may also be used to digitally sign a message (using the private key) and validate the signature (using the public key).</span></span>

<span data-ttu-id="61c55-252">Voir aussi *algorithme de clé publique*.</span><span class="sxs-lookup"><span data-stu-id="61c55-252">See also *public key algorithm*.</span></span>

</dd> </dl>

 

 



