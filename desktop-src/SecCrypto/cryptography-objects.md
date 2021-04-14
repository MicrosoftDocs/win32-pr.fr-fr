---
description: Répertorie les objets fournis par CryptoAPI.
ms.assetid: 4ab16355-1341-4c7a-b570-bd33f11dde00
title: Objets de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea3476e7edad1d32fe1e11635bd65622d2a8375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393504"
---
# <a name="cryptography-objects"></a><span data-ttu-id="bd483-103">Objets de chiffrement</span><span class="sxs-lookup"><span data-stu-id="bd483-103">Cryptography Objects</span></span>

<span data-ttu-id="bd483-104">Les objets de chiffrement sont catégorisés en fonction de l’utilisation comme suit :</span><span class="sxs-lookup"><span data-stu-id="bd483-104">Cryptography objects are categorized according to usage as follows:</span></span>

-   [<span data-ttu-id="bd483-105">Objets du magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="bd483-105">Certificate Store Objects</span></span>](#certificate-store-objects)
-   [<span data-ttu-id="bd483-106">Objets de signature numérique</span><span class="sxs-lookup"><span data-stu-id="bd483-106">Digital Signature Objects</span></span>](#digital-signature-objects)
-   [<span data-ttu-id="bd483-107">Objets de données enveloppés</span><span class="sxs-lookup"><span data-stu-id="bd483-107">Enveloped Data Objects</span></span>](#enveloped-data-objects)
-   [<span data-ttu-id="bd483-108">Objets de chiffrement de données</span><span class="sxs-lookup"><span data-stu-id="bd483-108">Data Encryption Objects</span></span>](#data-encryption-objects)
-   [<span data-ttu-id="bd483-109">Objets auxiliaires</span><span class="sxs-lookup"><span data-stu-id="bd483-109">Auxiliary Objects</span></span>](#auxiliary-objects)
-   [<span data-ttu-id="bd483-110">Objets d’inscription de certificat</span><span class="sxs-lookup"><span data-stu-id="bd483-110">Certificate Enrollment Objects</span></span>](#certificate-enrollment-objects)

## <a name="certificate-store-objects"></a><span data-ttu-id="bd483-111">Objets du magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="bd483-111">Certificate Store Objects</span></span>

<span data-ttu-id="bd483-112">Les objets suivants fonctionnent avec les [*magasins de certificats*](../secgloss/c-gly.md) et les certificats dans ces magasins.</span><span class="sxs-lookup"><span data-stu-id="bd483-112">The following objects work with [*certificate stores*](../secgloss/c-gly.md) and the certificates in those stores.</span></span> <span data-ttu-id="bd483-113">CAPICOM prend en charge l’utilisation de l’utilisateur actuel, de l’ordinateur local, de la mémoire et des magasins de certificats de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bd483-113">CAPICOM supports the use of Current User, Local Machine, memory, and Active Directory certificate stores.</span></span>



| <span data-ttu-id="bd483-114">Object</span><span class="sxs-lookup"><span data-stu-id="bd483-114">Object</span></span>                                             | <span data-ttu-id="bd483-115">Description</span><span class="sxs-lookup"><span data-stu-id="bd483-115">Description</span></span>                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd483-116">**Certificat**</span><span class="sxs-lookup"><span data-stu-id="bd483-116">**Certificate**</span></span>](certificate.md)                 | <span data-ttu-id="bd483-117">Un seul certificat numérique.</span><span class="sxs-lookup"><span data-stu-id="bd483-117">A single digital certificate.</span></span>                                                                                           |
| [<span data-ttu-id="bd483-118">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="bd483-118">**CertificatePolicies**</span></span>](certificatepolicies.md) | <span data-ttu-id="bd483-119">Collection d’objets [**PolicyInformation**](policyinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="bd483-119">A collection of [**PolicyInformation**](policyinformation.md) objects.</span></span>                                                 |
| [<span data-ttu-id="bd483-120">**Certificats**</span><span class="sxs-lookup"><span data-stu-id="bd483-120">**Certificates**</span></span>](certificates.md)               | <span data-ttu-id="bd483-121">Collection d’objets de [**certificat**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="bd483-121">Collection of [**Certificate**](certificate.md) objects.</span></span>                                                               |
| [<span data-ttu-id="bd483-122">**CertificateStatus**</span><span class="sxs-lookup"><span data-stu-id="bd483-122">**CertificateStatus**</span></span>](certificatestatus.md)     | <span data-ttu-id="bd483-123">Fournit des informations d’État sur un certificat.</span><span class="sxs-lookup"><span data-stu-id="bd483-123">Provides status information on a certificate.</span></span>                                                                           |
| [<span data-ttu-id="bd483-124">**Mutation**</span><span class="sxs-lookup"><span data-stu-id="bd483-124">**Chain**</span></span>](chain.md)                             | <span data-ttu-id="bd483-125">Crée et vérifie une chaîne de validation de certificat sur la base d’un certificat numérique.</span><span class="sxs-lookup"><span data-stu-id="bd483-125">Creates and checks a certificate validation chain based on a digital certificate.</span></span>                                       |
| [<span data-ttu-id="bd483-126">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="bd483-126">**ExtendedProperties**</span></span>](extendedproperties.md)   | <span data-ttu-id="bd483-127">Représente une collection d’objets [**ExtendedProperty**](extendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="bd483-127">Represents a collection of [**ExtendedProperty**](extendedproperty.md) objects.</span></span>                                        |
| [<span data-ttu-id="bd483-128">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="bd483-128">**ExtendedProperty**</span></span>](extendedproperties.md)     | <span data-ttu-id="bd483-129">Représente une propriété étendue Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bd483-129">Represents a Microsoft-extended property.</span></span>                                                                               |
| [<span data-ttu-id="bd483-130">**Extension**</span><span class="sxs-lookup"><span data-stu-id="bd483-130">**Extension**</span></span>](extension.md)                     | <span data-ttu-id="bd483-131">Représente une extension de certificat unique.</span><span class="sxs-lookup"><span data-stu-id="bd483-131">Represents a single certificate extension.</span></span>                                                                              |
| [<span data-ttu-id="bd483-132">**Extensions**</span><span class="sxs-lookup"><span data-stu-id="bd483-132">**Extensions**</span></span>](extensions.md)                   | <span data-ttu-id="bd483-133">Représente une collection d’objets d' [**extension**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="bd483-133">Represents a collection of [**Extension**](extension.md) objects.</span></span>                                                      |
| [<span data-ttu-id="bd483-134">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="bd483-134">**PrivateKey**</span></span>](privatekey.md)                   | <span data-ttu-id="bd483-135">Représente une clé privée.</span><span class="sxs-lookup"><span data-stu-id="bd483-135">Represents a private key.</span></span>                                                                                               |
| [<span data-ttu-id="bd483-136">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="bd483-136">**PublicKey**</span></span>](publickey.md)                     | <span data-ttu-id="bd483-137">Représente une clé publique dans un objet de [**certificat**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="bd483-137">Represents a public key in a [**Certificate**](certificate.md) object.</span></span>                                                 |
| [<span data-ttu-id="bd483-138">**Magasin**</span><span class="sxs-lookup"><span data-stu-id="bd483-138">**Store**</span></span>](store.md)                             | <span data-ttu-id="bd483-139">Fournit les propriétés et les méthodes permettant de choisir, gérer et utiliser les magasins de certificats et les certificats dans ces magasins.</span><span class="sxs-lookup"><span data-stu-id="bd483-139">Provides the properties and methods to choose, manage, and use certificate stores and the certificates in those stores.</span></span> |
| [<span data-ttu-id="bd483-140">**Modèle**</span><span class="sxs-lookup"><span data-stu-id="bd483-140">**Template**</span></span>](template.md)                       | <span data-ttu-id="bd483-141">Représente le modèle d’extension de certificat du certificat.</span><span class="sxs-lookup"><span data-stu-id="bd483-141">Represents the certificate extension template of the certificate.</span></span>                                                       |



 

## <a name="digital-signature-objects"></a><span data-ttu-id="bd483-142">Objets de signature numérique</span><span class="sxs-lookup"><span data-stu-id="bd483-142">Digital Signature Objects</span></span>

<span data-ttu-id="bd483-143">Les objets suivants sont exportés pour signer numériquement les données et pour vérifier les signatures numériques.</span><span class="sxs-lookup"><span data-stu-id="bd483-143">The following objects are exported to digitally sign data and to verify digital signatures.</span></span>



| <span data-ttu-id="bd483-144">Object</span><span class="sxs-lookup"><span data-stu-id="bd483-144">Object</span></span>                           | <span data-ttu-id="bd483-145">Description</span><span class="sxs-lookup"><span data-stu-id="bd483-145">Description</span></span>                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd483-146">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="bd483-146">**SignedCode**</span></span>](signedcode.md) | <span data-ttu-id="bd483-147">Objet utilisé pour signer du code avec une signature numérique Authenticode et pour vérifier la signature du code signé.</span><span class="sxs-lookup"><span data-stu-id="bd483-147">Object used to sign code with an Authenticode digital signature and to verify the signature on signed code.</span></span> |
| [<span data-ttu-id="bd483-148">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="bd483-148">**SignedData**</span></span>](signeddata.md) | <span data-ttu-id="bd483-149">Objet utilisé pour signer des données et vérifier la signature sur les données signées.</span><span class="sxs-lookup"><span data-stu-id="bd483-149">Object used to sign data and to verify the signature on signed data.</span></span>                                        |
| [<span data-ttu-id="bd483-150">**Signataire**</span><span class="sxs-lookup"><span data-stu-id="bd483-150">**Signer**</span></span>](signer.md)         | <span data-ttu-id="bd483-151">Informations sur un seul signataire de données, y compris le certificat du signataire.</span><span class="sxs-lookup"><span data-stu-id="bd483-151">Information on a single data signer, including the signer's certificate.</span></span>                                    |
| [<span data-ttu-id="bd483-152">**Signataires**</span><span class="sxs-lookup"><span data-stu-id="bd483-152">**Signers**</span></span>](signers.md)       | <span data-ttu-id="bd483-153">Collection d’objets [**signataires**](signer.md) .</span><span class="sxs-lookup"><span data-stu-id="bd483-153">Collection of [**Signer**](signer.md) objects.</span></span>                                                             |



 

## <a name="enveloped-data-objects"></a><span data-ttu-id="bd483-154">Objets de données enveloppés</span><span class="sxs-lookup"><span data-stu-id="bd483-154">Enveloped Data Objects</span></span>

<span data-ttu-id="bd483-155">Les objets suivants sont exportés pour créer des messages de données enveloppés pour la confidentialité et pour déchiffrer des données dans des messages enveloppés.</span><span class="sxs-lookup"><span data-stu-id="bd483-155">The following objects are exported to create enveloped data messages for privacy and to decrypt data in enveloped messages.</span></span>



| <span data-ttu-id="bd483-156">Object</span><span class="sxs-lookup"><span data-stu-id="bd483-156">Object</span></span>                                 | <span data-ttu-id="bd483-157">Description</span><span class="sxs-lookup"><span data-stu-id="bd483-157">Description</span></span>                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd483-158">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="bd483-158">**EnvelopedData**</span></span>](envelopeddata.md) | <span data-ttu-id="bd483-159">Objets utilisés pour créer, envoyer et recevoir des données enveloppées.</span><span class="sxs-lookup"><span data-stu-id="bd483-159">Objects used to create, send, and receive enveloped data.</span></span> <span data-ttu-id="bd483-160">Les données enveloppées sont chiffrées afin que seuls les destinataires prévus puissent les déchiffrer.</span><span class="sxs-lookup"><span data-stu-id="bd483-160">Enveloped data is encrypted so that only the intended recipients can decrypt it.</span></span> |
| [<span data-ttu-id="bd483-161">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="bd483-161">**Recipients**</span></span>](recipients.md)       | <span data-ttu-id="bd483-162">Collection d’objets de [**certificat**](certificate.md) des destinataires prévus d’un message enveloppé.</span><span class="sxs-lookup"><span data-stu-id="bd483-162">Collection of the [**Certificate**](certificate.md) objects of the intended recipients of an enveloped message.</span></span>                           |



 

## <a name="data-encryption-objects"></a><span data-ttu-id="bd483-163">Objets de chiffrement de données</span><span class="sxs-lookup"><span data-stu-id="bd483-163">Data Encryption Objects</span></span>

<span data-ttu-id="bd483-164">L’objet suivant est exporté pour chiffrer les données arbitraires pour la confidentialité et déchiffrer les données chiffrées.</span><span class="sxs-lookup"><span data-stu-id="bd483-164">The following object is exported to encrypt arbitrary data for privacy and to decrypt encrypted data.</span></span>



| <span data-ttu-id="bd483-165">Object</span><span class="sxs-lookup"><span data-stu-id="bd483-165">Object</span></span>                                 | <span data-ttu-id="bd483-166">Description</span><span class="sxs-lookup"><span data-stu-id="bd483-166">Description</span></span>                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd483-167">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="bd483-167">**EncryptedData**</span></span>](encrypteddata.md) | <span data-ttu-id="bd483-168">Objets utilisés pour chiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="bd483-168">Objects used to encrypt data.</span></span> <span data-ttu-id="bd483-169">Les données chiffrées dans un objet [**EncryptedData**](encrypteddata.md) peuvent être déchiffrées.</span><span class="sxs-lookup"><span data-stu-id="bd483-169">Encrypted data in an [**EncryptedData**](encrypteddata.md) object can be decrypted.</span></span> |



 

## <a name="auxiliary-objects"></a><span data-ttu-id="bd483-170">Objets auxiliaires</span><span class="sxs-lookup"><span data-stu-id="bd483-170">Auxiliary Objects</span></span>

<span data-ttu-id="bd483-171">Les objets suivants sont exportés pour modifier les comportements par défaut d’autres objets et pour gérer les certificats, les magasins de certificats et les messages.</span><span class="sxs-lookup"><span data-stu-id="bd483-171">The following objects are exported to change default behaviors of other objects and to manage certificates, certificate stores, and messages.</span></span>



| <span data-ttu-id="bd483-172">Object</span><span class="sxs-lookup"><span data-stu-id="bd483-172">Object</span></span>                                         | <span data-ttu-id="bd483-173">Description</span><span class="sxs-lookup"><span data-stu-id="bd483-173">Description</span></span>                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd483-174">**Algorithme**</span><span class="sxs-lookup"><span data-stu-id="bd483-174">**Algorithm**</span></span>](algorithm.md)                 | <span data-ttu-id="bd483-175">Définit la longueur de l’algorithme et de la [*clé*](../secgloss/k-gly.md) à utiliser dans les opérations de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="bd483-175">Sets the algorithm and [*key length*](../secgloss/k-gly.md) to be used in cryptographic operations.</span></span> |
| [<span data-ttu-id="bd483-176">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bd483-176">**Attribute**</span></span>](attribute.md)                 | <span data-ttu-id="bd483-177">Fournit une seule partie des informations ajoutées sur une signature, telles que l’heure de la signature.</span><span class="sxs-lookup"><span data-stu-id="bd483-177">Provides a single piece of added information about a signature, such as the time of signing.</span></span>                                                    |
| [<span data-ttu-id="bd483-178">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="bd483-178">**Attributes**</span></span>](attributes.md)               | <span data-ttu-id="bd483-179">Collection d’objets [**attribute**](attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="bd483-179">Collection of [**Attribute**](attribute.md) objects.</span></span>                                                                                           |
| [<span data-ttu-id="bd483-180">**BasicConstraints**</span><span class="sxs-lookup"><span data-stu-id="bd483-180">**BasicConstraints**</span></span>](basicconstraints.md)   | <span data-ttu-id="bd483-181">Fournit un accès en lecture seule aux contraintes de base sur les utilisations d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="bd483-181">Provides read-only access to basic constraints on the uses of a certificate.</span></span>                                                                    |
| [<span data-ttu-id="bd483-182">**EKU**</span><span class="sxs-lookup"><span data-stu-id="bd483-182">**EKU**</span></span>](eku.md)                             | <span data-ttu-id="bd483-183">Fournit l’accès aux propriétés EKU des certificats.</span><span class="sxs-lookup"><span data-stu-id="bd483-183">Provides access to EKU properties of certificates.</span></span>                                                                                              |
| [<span data-ttu-id="bd483-184">**Utilisations améliorées de la clé**</span><span class="sxs-lookup"><span data-stu-id="bd483-184">**EKUs**</span></span>](ekus.md)                           | <span data-ttu-id="bd483-185">Collection d’objets [**EKU**](eku.md) .</span><span class="sxs-lookup"><span data-stu-id="bd483-185">Collection of [**EKU**](eku.md) objects.</span></span>                                                                                                       |
| [<span data-ttu-id="bd483-186">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="bd483-186">**EncodedData**</span></span>](encodeddata.md)             | <span data-ttu-id="bd483-187">Représente un bloc de données encodées.</span><span class="sxs-lookup"><span data-stu-id="bd483-187">Represents a block of encoded data.</span></span>                                                                                                             |
| [<span data-ttu-id="bd483-188">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="bd483-188">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)   | <span data-ttu-id="bd483-189">Fournit un accès en lecture seule aux propriétés d’utilisation de clé étendue des certificats.</span><span class="sxs-lookup"><span data-stu-id="bd483-189">Provides read-only access to the extended key usage properties of certificates.</span></span>                                                                 |
| [<span data-ttu-id="bd483-190">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="bd483-190">**HashedData**</span></span>](hasheddata.md)               | <span data-ttu-id="bd483-191">Fournit les fonctionnalités permettant d’appliquer un algorithme de hachage à une chaîne.</span><span class="sxs-lookup"><span data-stu-id="bd483-191">Provides functionality for applying a hash algorithm to a string.</span></span>                                                                               |
| [<span data-ttu-id="bd483-192">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="bd483-192">**KeyUsage**</span></span>](keyusage.md)                   | <span data-ttu-id="bd483-193">Fournit un accès en lecture seule aux propriétés d’utilisation de clé des certificats.</span><span class="sxs-lookup"><span data-stu-id="bd483-193">Provides read-only access to key usage properties of certificates.</span></span>                                                                              |
| [<span data-ttu-id="bd483-194">**NoticeNumbers**</span><span class="sxs-lookup"><span data-stu-id="bd483-194">**NoticeNumbers**</span></span>](noticenumbers.md)         | <span data-ttu-id="bd483-195">Représente une collection d’objets d' [**extension**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="bd483-195">Represents a collection of [**Extension**](extension.md) objects.</span></span>                                                                              |
| [<span data-ttu-id="bd483-196">**OID**</span><span class="sxs-lookup"><span data-stu-id="bd483-196">**OID**</span></span>](oid.md)                             | <span data-ttu-id="bd483-197">Représente un identificateur d’objet qui est utilisé par plusieurs propriétés CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="bd483-197">Represents an object identifier that is used by several CAPICOM properties.</span></span>                                                                     |
| [<span data-ttu-id="bd483-198">**OID**</span><span class="sxs-lookup"><span data-stu-id="bd483-198">**OIDs**</span></span>](oids.md)                           | <span data-ttu-id="bd483-199">Représente une collection d’objets [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="bd483-199">Represents a collection of [**OID**](oid.md) objects.</span></span>                                                                                          |
| [<span data-ttu-id="bd483-200">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="bd483-200">**PolicyInformation**</span></span>](policyinformation.md) | <span data-ttu-id="bd483-201">Fournit l’accès aux OID de stratégie d’une extension.</span><span class="sxs-lookup"><span data-stu-id="bd483-201">Provides access to the policy OIDs of an extension.</span></span>                                                                                             |
| [<span data-ttu-id="bd483-202">**Qualificateur**</span><span class="sxs-lookup"><span data-stu-id="bd483-202">**Qualifier**</span></span>](qualifier.md)                 | <span data-ttu-id="bd483-203">Représente un pointeur CPS (certification Practice Statement) ou un qualificateur d’avis utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd483-203">Represents a Certification Practice Statement (CPS) pointer or user notice qualifier.</span></span>                                                           |
| [<span data-ttu-id="bd483-204">**Qualificateurs**</span><span class="sxs-lookup"><span data-stu-id="bd483-204">**Qualifiers**</span></span>](qualifiers.md)               | <span data-ttu-id="bd483-205">Représente une collection de qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="bd483-205">Represents a collection of qualifiers.</span></span>                                                                                                          |
| [<span data-ttu-id="bd483-206">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="bd483-206">**Settings**</span></span>](settings.md)                   | <span data-ttu-id="bd483-207">Active ou désactive les boîtes de dialogue pour demander l’identité de l’expéditeur ou du signataire si cette identité n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bd483-207">Enables or disables dialog boxes to prompt for signer or sender identity if that identity is not specified.</span></span>                                     |
| [<span data-ttu-id="bd483-208">**Services**</span><span class="sxs-lookup"><span data-stu-id="bd483-208">**Utilities**</span></span>](utilities.md)                 | <span data-ttu-id="bd483-209">Fournit des fonctionnalités pour les tâches courantes.</span><span class="sxs-lookup"><span data-stu-id="bd483-209">Provides functionality for common tasks.</span></span>                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a><span data-ttu-id="bd483-210">Objets d’inscription de certificat</span><span class="sxs-lookup"><span data-stu-id="bd483-210">Certificate Enrollment Objects</span></span>

<span data-ttu-id="bd483-211">L’objet suivant est utilisé pour l’inscription de certificats.</span><span class="sxs-lookup"><span data-stu-id="bd483-211">The following object is used for certificate enrollment.</span></span>



| <span data-ttu-id="bd483-212">Object</span><span class="sxs-lookup"><span data-stu-id="bd483-212">Object</span></span>                     | <span data-ttu-id="bd483-213">Description</span><span class="sxs-lookup"><span data-stu-id="bd483-213">Description</span></span>                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd483-214">[**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bd483-214">[**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))</span></span> | <span data-ttu-id="bd483-215">Objet qui représente le contrôle d’inscription de certificat.</span><span class="sxs-lookup"><span data-stu-id="bd483-215">Object that represents the Certificate Enrollment Control.</span></span> <span data-ttu-id="bd483-216">Il est principalement utilisé lors de la programmation dans Visual Basic ou dans un autre langage Automation.</span><span class="sxs-lookup"><span data-stu-id="bd483-216">It is primarily used when programming in Visual Basic or another Automation language.</span></span> |



 

 

 
