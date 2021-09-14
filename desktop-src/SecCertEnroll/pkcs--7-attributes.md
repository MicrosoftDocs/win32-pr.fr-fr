---
description: PKCS \# 7 est une norme de syntaxe de message de chiffrement.
ms.assetid: fd4e2a13-f257-4ba9-a11d-35f49c5a6c00
title: '\#Attributs PKCS 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0c7bc9b991a6625cae36ae9857275a9d86786a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121134"
---
# <a name="pkcs-7-attributes"></a>\#Attributs PKCS 7

PKCS \# 7 est une norme de syntaxe de message de chiffrement. Un \# message PKCS 7 ne constitue pas, en soi, une demande de certificat, mais il peut encapsuler une \# demande PKCS 10 ou CMC dans une structure de programme ASN. 1 **ContentInfo** en utilisant l’un des types de contenu suivants. L’encapsulation vous permet d’ajouter des fonctionnalités supplémentaires, telles que plusieurs signatures, qui ne sont pas disponibles dans le cas contraire.

-   **Données**
-   **SignedData**
-   **EnvelopedData**
-   **SignedAndEnvelopedData**
-   **DigestedData**
-   **EncryptedData**

Les attributs peuvent être ajoutés aux champs **authenticatedAttributes** et **unauthenticatedAttributes** du type de contenu **SignedData** .

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

Le processus requis pour archiver la clé privée d’un client sur une autorité de certification (CA) fournit un exemple complet de la façon dont les attributs authentifiés (signés) et les attributs non authentifiés peuvent être utilisés :

-   Le client crée un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) et ajoute des données appropriées pour le type de certificat demandé.
-   Le client utilise la \# requête PKCS 10 pour initialiser un objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) . La \# requête PKCS 10 est placée dans la structure **TaggedRequest** de la demande CMC. Pour plus d’informations, consultez [attributs CMC](cmc-attributes.md).
-   Le client chiffre une clé privée et l’utilise pour initialiser un objet [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) . Le nouvel attribut **ArchiveKey** est encapsulé dans une structure **EnvelopedData** .

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

-   Le client crée un hachage SHA-1 de la clé chiffrée et l’utilise pour initialiser un objet [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) .
-   Le client récupère la collection [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) à partir de la demande CMC et lui ajoute les attributs **ArchiveKey** et **ArchiveKeyHash** . Les attributs sont placés dans la structure **TaggedAttributes** de la demande CMC.
-   Le client utilise la demande CMC pour initialiser un objet [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) . Cela place la demande CMC dans le champ **ContentInfo** de la \# structure PKCS 7 **SignedData** .
-   L’attribut **ArchiveKeyHash** est signé et placé dans la séquence **authenticatedAttributes** de la structure **signataires** .
-   L’attribut **ArchiveKey** est placé dans la séquence **unauthenticatedAttributes** de la structure **signataires** associée au signataire principal du message PKCS \# 7.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs pris en charge](supported-attributes.md)
</dt> </dl>

 

 



