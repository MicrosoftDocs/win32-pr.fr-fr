---
description: Le chiffrement à clé publique s’appuie sur une paire de clés publique et privée pour chiffrer et déchiffrer le contenu.
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: Certificats de clé publique X. 509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acd602e9b47cb7825f6d75df0fb74399b914db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562484"
---
# <a name="x509-public-key-certificates"></a><span data-ttu-id="7437a-103">Certificats de clé publique X. 509</span><span class="sxs-lookup"><span data-stu-id="7437a-103">X.509 Public Key Certificates</span></span>

<span data-ttu-id="7437a-104">Le chiffrement à clé publique s’appuie sur une paire de clés publique et privée pour chiffrer et déchiffrer le contenu.</span><span class="sxs-lookup"><span data-stu-id="7437a-104">Public key cryptography relies on a public and private key pair to encrypt and decrypt content.</span></span> <span data-ttu-id="7437a-105">Les clés sont liées mathématiquement, et le contenu chiffré à l’aide de l’une des clés ne peut être déchiffré qu’à l’aide de l’autre.</span><span class="sxs-lookup"><span data-stu-id="7437a-105">The keys are mathematically related, and content encrypted by using one of the keys can only be decrypted by using the other.</span></span> <span data-ttu-id="7437a-106">La clé privée est gardée secrète.</span><span class="sxs-lookup"><span data-stu-id="7437a-106">The private key is kept secret.</span></span> <span data-ttu-id="7437a-107">La clé publique est généralement incorporée dans un certificat binaire, et le certificat est publié dans une base de données accessible par tous les utilisateurs autorisés.</span><span class="sxs-lookup"><span data-stu-id="7437a-107">The public key is typically embedded in a binary certificate, and the certificate is published to a database that can be reached by all authorized users.</span></span>

<span data-ttu-id="7437a-108">La norme de l’infrastructure à clé publique (PKI) X. 509 identifie la configuration requise pour les certificats de clé publique robustes.</span><span class="sxs-lookup"><span data-stu-id="7437a-108">The X.509 public key infrastructure (PKI) standard identifies the requirements for robust public key certificates.</span></span> <span data-ttu-id="7437a-109">Un certificat est une structure de données signée qui lie une clé publique à une personne, un ordinateur ou une organisation.</span><span class="sxs-lookup"><span data-stu-id="7437a-109">A certificate is a signed data structure that binds a public key to a person, computer, or organization.</span></span> <span data-ttu-id="7437a-110">Les certificats sont émis par des [*autorités de certification*](/windows/desktop/SecGloss/c-gly) (ca).</span><span class="sxs-lookup"><span data-stu-id="7437a-110">Certificates are issued by [*certification authorities*](/windows/desktop/SecGloss/c-gly) (CAs).</span></span> <span data-ttu-id="7437a-111">Toutes les personnes qui sont parties à sécuriser les communications qui utilisent une clé publique s’appuient sur l’autorité de certification pour vérifier correctement les identités des personnes, des systèmes ou des entités auxquels elle émet des certificats.</span><span class="sxs-lookup"><span data-stu-id="7437a-111">All who are party to secure communications that make use of a public key rely on the CA to adequately verify the identities of the individuals, systems, or entities to which it issues certificates.</span></span> <span data-ttu-id="7437a-112">Le niveau de vérification dépend généralement du niveau de sécurité requis pour la transaction.</span><span class="sxs-lookup"><span data-stu-id="7437a-112">The level of verification typically depends on the level of security required for the transaction.</span></span> <span data-ttu-id="7437a-113">Si l’autorité de certification peut vérifier correctement l’identité du demandeur, il signe (chiffre), encode et émet le certificat.</span><span class="sxs-lookup"><span data-stu-id="7437a-113">If the CA can suitably verify the identity of the requester, it signs (encrypts), encodes, and issues the certificate.</span></span>

<span data-ttu-id="7437a-114">Un certificat est une structure de données signée qui lie une clé publique à une entité.</span><span class="sxs-lookup"><span data-stu-id="7437a-114">A certificate is a signed data structure that binds a public key to an entity.</span></span> <span data-ttu-id="7437a-115">La syntaxe ASN. 1 ( [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) ) pour le certificat [*X. 509*](/windows/desktop/SecGloss/x-gly) version 3 est présentée dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="7437a-115">The [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) syntax for the version 3 [*X.509*](/windows/desktop/SecGloss/x-gly) certificate is shown in the following example.</span></span>

``` syntax
-- X.509 signed certificate 

SignedContent ::= SEQUENCE 
{
  certificate         CertificateToBeSigned,
  algorithm           Object Identifier,
  signature           BITSTRING
}
 
-- X.509 certificate to be signed

CertificateToBeSigned ::= SEQUENCE 
{
  version                 [0] CertificateVersion DEFAULT v1,
  serialNumber            CertificateSerialNumber,
  signature               AlgorithmIdentifier,
  issuer                  Name
  validity                Validity,
  subject                 Name
  subjectPublicKeyInfo    SubjectPublicKeyInfo,
  issuerUniqueIdentifier  [1] IMPLICIT UniqueIdentifier OPTIONAL,
  subjectUniqueIdentifier [2] IMPLICIT UniqueIdentifier OPTIONAL,
  extensions              [3] Extensions OPTIONAL
}
```

<span data-ttu-id="7437a-116">Depuis sa création dans 1998, trois versions de la norme de certificat de clé publique X. 509 ont évolué.</span><span class="sxs-lookup"><span data-stu-id="7437a-116">Since its inception in 1998, three versions of the X.509 public key certificate standard have evolved.</span></span> <span data-ttu-id="7437a-117">Comme indiqué dans l’illustration suivante, chaque version successive de la structure de données a conservé les champs qui existaient dans les versions précédentes et en a ajouté davantage.</span><span class="sxs-lookup"><span data-stu-id="7437a-117">As shown by the following illustration, each successive version of the data structure has retained the fields that existed in the previous versions and added more.</span></span>

![certificats x. 509 versions 1, 2 et 3](images/x509certificateversions.png)

<span data-ttu-id="7437a-119">Les rubriques suivantes décrivent les champs disponibles plus en détail :</span><span class="sxs-lookup"><span data-stu-id="7437a-119">The following topics discuss the available fields in more detail:</span></span>

-   [<span data-ttu-id="7437a-120">Champs de base</span><span class="sxs-lookup"><span data-stu-id="7437a-120">Basic Fields</span></span>](about-basic-fields.md)
-   [<span data-ttu-id="7437a-121">Champs de la version 2</span><span class="sxs-lookup"><span data-stu-id="7437a-121">Version 2 Fields</span></span>](about-version-2-fields.md)
-   [<span data-ttu-id="7437a-122">Extensions de la version 3</span><span class="sxs-lookup"><span data-stu-id="7437a-122">Version 3 Extensions</span></span>](about-version-3-extensions.md)

## <a name="related-topics"></a><span data-ttu-id="7437a-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7437a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7437a-124">Infrastructure à clé publique (PKI)</span><span class="sxs-lookup"><span data-stu-id="7437a-124">Public Key Infrastructure</span></span>](public-key-infrastructure.md)
</dt> </dl>

 

 
