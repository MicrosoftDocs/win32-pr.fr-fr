---
description: PKCS \# 7 est une norme de syntaxe de message de chiffrement.
ms.assetid: fd4e2a13-f257-4ba9-a11d-35f49c5a6c00
title: '\#Attributs PKCS 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0c7bc9b991a6625cae36ae9857275a9d86786a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545040"
---
# <a name="pkcs-7-attributes"></a><span data-ttu-id="52afe-103">\#Attributs PKCS 7</span><span class="sxs-lookup"><span data-stu-id="52afe-103">PKCS \#7 Attributes</span></span>

<span data-ttu-id="52afe-104">PKCS \# 7 est une norme de syntaxe de message de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="52afe-104">PKCS \#7 is a cryptographic message syntax standard.</span></span> <span data-ttu-id="52afe-105">Un \# message PKCS 7 ne constitue pas, en soi, une demande de certificat, mais il peut encapsuler une \# demande PKCS 10 ou CMC dans une structure de programme ASN. 1 **ContentInfo** en utilisant l’un des types de contenu suivants.</span><span class="sxs-lookup"><span data-stu-id="52afe-105">A PKCS \#7 message does not, by itself, constitute a certificate request, but it can encapsulate a PKCS \#10 or CMC request in a **ContentInfo** ASN.1 structure by using one of the following content types.</span></span> <span data-ttu-id="52afe-106">L’encapsulation vous permet d’ajouter des fonctionnalités supplémentaires, telles que plusieurs signatures, qui ne sont pas disponibles dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="52afe-106">Encapsulation enables you to add extra functionality, such as multiple signatures, that is not otherwise available.</span></span>

-   <span data-ttu-id="52afe-107">**Données**</span><span class="sxs-lookup"><span data-stu-id="52afe-107">**Data**</span></span>
-   <span data-ttu-id="52afe-108">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="52afe-108">**SignedData**</span></span>
-   <span data-ttu-id="52afe-109">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="52afe-109">**EnvelopedData**</span></span>
-   <span data-ttu-id="52afe-110">**SignedAndEnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="52afe-110">**SignedAndEnvelopedData**</span></span>
-   <span data-ttu-id="52afe-111">**DigestedData**</span><span class="sxs-lookup"><span data-stu-id="52afe-111">**DigestedData**</span></span>
-   <span data-ttu-id="52afe-112">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="52afe-112">**EncryptedData**</span></span>

<span data-ttu-id="52afe-113">Les attributs peuvent être ajoutés aux champs **authenticatedAttributes** et **unauthenticatedAttributes** du type de contenu **SignedData** .</span><span class="sxs-lookup"><span data-stu-id="52afe-113">Attributes can be added to the **authenticatedAttributes** and **unauthenticatedAttributes** fields of the **SignedData** content type.</span></span>

``` syntax
SignedData ::= SEQUENCE 
{
   version             INTEGER,
   digestAlgorithms    DigestAlgorithmIdentifiers,
   contentInfo         ContentInfo,
   certificates        [0] IMPLICIT Certificates OPTIONAL,
   crls                [1] IMPLICIT CertificateRevocationLists OPTIONAL,
   signerInfos         SignerInfos
}

SignerInfos ::= SET OF SignerInfo

SignerInfo ::= SEQUENCE 
{
    version                     INTEGER,
    sid                         CertIdentifier,
    digestAlgorithm             DigestAlgorithmIdentifier,
    authenticatedAttributes     [0] IMPLICIT Attributes OPTIONAL,
    digestEncryptionAlgorithm   DigestEncryptionAlgId,
    encryptedDigest             EncryptedDigest,
    unauthenticatedAttributes   [1] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

<span data-ttu-id="52afe-114">Le processus requis pour archiver la clé privée d’un client sur une autorité de certification (CA) fournit un exemple complet de la façon dont les attributs authentifiés (signés) et les attributs non authentifiés peuvent être utilisés :</span><span class="sxs-lookup"><span data-stu-id="52afe-114">The process required to archive a client's private key on a certification authority (CA) provides a comprehensive example of how authenticated (signed) attributes and the unauthenticated attributes can be used:</span></span>

-   <span data-ttu-id="52afe-115">Le client crée un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) et ajoute des données appropriées pour le type de certificat demandé.</span><span class="sxs-lookup"><span data-stu-id="52afe-115">The client creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and adds appropriate data for the type of certificate being requested.</span></span>
-   <span data-ttu-id="52afe-116">Le client utilise la \# requête PKCS 10 pour initialiser un objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="52afe-116">The client uses the PKCS \#10 request to initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span> <span data-ttu-id="52afe-117">La \# requête PKCS 10 est placée dans la structure **TaggedRequest** de la demande CMC.</span><span class="sxs-lookup"><span data-stu-id="52afe-117">The PKCS \#10 request is placed into the **TaggedRequest** structure in the CMC request.</span></span> <span data-ttu-id="52afe-118">Pour plus d’informations, consultez [attributs CMC](cmc-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="52afe-118">For more information, see [CMC Attributes](cmc-attributes.md).</span></span>
-   <span data-ttu-id="52afe-119">Le client chiffre une clé privée et l’utilise pour initialiser un objet [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) .</span><span class="sxs-lookup"><span data-stu-id="52afe-119">The client encrypts a private key and uses it to initialize an [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) object.</span></span> <span data-ttu-id="52afe-120">Le nouvel attribut **ArchiveKey** est encapsulé dans une structure **EnvelopedData** .</span><span class="sxs-lookup"><span data-stu-id="52afe-120">The new **ArchiveKey** attribute is encapsulated in an **EnvelopedData** structure.</span></span>

    ``` syntax
    EnvelopedData ::= SEQUENCE 
    {
        version                 INTEGER,
        recipientInfos          RecipientInfos,
        encryptedContentInfo    EncryptedContentInfo
    } 

    RecipientInfos ::= SET OF RecipientInfo

    EncryptedContentInfo ::= SEQUENCE 
    {
        contentType                 ContentType,
        contentEncryptionAlgorithm  ContentEncryptionAlgId,
        encryptedContent            [0] IMPLICIT EncryptedContent OPTIONAL
    } 

    EncryptedContent ::= OCTET STRING

    RecipientInfo ::= SEQUENCE 
    {
        version                 INTEGER,
        issuerAndSerialNumber   IssuerAndSerialNumber,
        keyEncryptionAlgorithm  KeyEncryptionAlgId,
        encryptedKey            EncryptedKey
    } 
    ```

-   <span data-ttu-id="52afe-121">Le client crée un hachage SHA-1 de la clé chiffrée et l’utilise pour initialiser un objet [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) .</span><span class="sxs-lookup"><span data-stu-id="52afe-121">The client creates a SHA-1 hash of the encrypted key and uses it to initialize an [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) object.</span></span>
-   <span data-ttu-id="52afe-122">Le client récupère la collection [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) à partir de la demande CMC et lui ajoute les attributs **ArchiveKey** et **ArchiveKeyHash** .</span><span class="sxs-lookup"><span data-stu-id="52afe-122">The client retrieves the [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) collection from the CMC request and adds the **ArchiveKey** and the **ArchiveKeyHash** attributes to it.</span></span> <span data-ttu-id="52afe-123">Les attributs sont placés dans la structure **TaggedAttributes** de la demande CMC.</span><span class="sxs-lookup"><span data-stu-id="52afe-123">The attributes are placed into the **TaggedAttributes** structure of the CMC request.</span></span>
-   <span data-ttu-id="52afe-124">Le client utilise la demande CMC pour initialiser un objet [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) .</span><span class="sxs-lookup"><span data-stu-id="52afe-124">The client uses the CMC request to initialize an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object.</span></span> <span data-ttu-id="52afe-125">Cela place la demande CMC dans le champ **ContentInfo** de la \# structure PKCS 7 **SignedData** .</span><span class="sxs-lookup"><span data-stu-id="52afe-125">This places the CMC request into the **contentInfo** field of the PKCS \#7 **SignedData** structure.</span></span>
-   <span data-ttu-id="52afe-126">L’attribut **ArchiveKeyHash** est signé et placé dans la séquence **authenticatedAttributes** de la structure **signataires** .</span><span class="sxs-lookup"><span data-stu-id="52afe-126">The **ArchiveKeyHash** attribute is signed and placed in the **authenticatedAttributes** sequence of the **SignerInfo** structure.</span></span>
-   <span data-ttu-id="52afe-127">L’attribut **ArchiveKey** est placé dans la séquence **unauthenticatedAttributes** de la structure **signataires** associée au signataire principal du message PKCS \# 7.</span><span class="sxs-lookup"><span data-stu-id="52afe-127">The **ArchiveKey** attribute is placed in the **unauthenticatedAttributes** sequence of the **SignerInfo** structure associated with the primary signer of the PKCS \#7 message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52afe-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52afe-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52afe-129">Attributs pris en charge</span><span class="sxs-lookup"><span data-stu-id="52afe-129">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



