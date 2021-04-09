---
description: Un certificat X. 509 version 1 contient les champs suivants. Les champs de la version 2 sont abordés dans les champs de la version 2. Les champs de la version 3 sont traités dans les extensions de la version 3.
ms.assetid: d614130c-cf1b-4580-8903-064982ed738e
title: Champs de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad24afa21787227b3fe47ab187a97c7886c9c9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865037"
---
# <a name="basic-fields"></a><span data-ttu-id="029e0-105">Champs de base</span><span class="sxs-lookup"><span data-stu-id="029e0-105">Basic Fields</span></span>

<span data-ttu-id="029e0-106">Un certificat X. 509 version 1 contient les champs suivants.</span><span class="sxs-lookup"><span data-stu-id="029e0-106">An X.509 version 1 certificate contains the following fields.</span></span> <span data-ttu-id="029e0-107">Les champs de la version 2 sont abordés dans les champs de la [version 2](about-version-2-fields.md).</span><span class="sxs-lookup"><span data-stu-id="029e0-107">Version 2 fields are discussed in [Version 2 Fields](about-version-2-fields.md).</span></span> <span data-ttu-id="029e0-108">Les champs de la version 3 sont traités dans les extensions de la [version 3](about-version-3-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="029e0-108">Version 3 fields are discussed in [Version 3 Extensions](about-version-3-extensions.md).</span></span>

## <a name="version"></a><span data-ttu-id="029e0-109">Version</span><span class="sxs-lookup"><span data-stu-id="029e0-109">Version</span></span>

<span data-ttu-id="029e0-110">Indique le numéro de version du certificat encodé.</span><span class="sxs-lookup"><span data-stu-id="029e0-110">Specifies the version number of the encoded certificate.</span></span> <span data-ttu-id="029e0-111">Actuellement, les valeurs possibles de ce champ sont 0, 1 ou 2, mais cela peut être développé à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="029e0-111">Currently, the possible values of this field are 0, 1, or 2, but this may be expanded in the future.</span></span>

``` syntax
---------------------------------------------------------------------
-- Version number. Currently, this can be 0, 1, or 2.
---------------------------------------------------------------------
CertificateVersion ::= INTEGER {v1(0), v2(1), v3(2)}
```

## <a name="serial-number"></a><span data-ttu-id="029e0-112">Numéro de série</span><span class="sxs-lookup"><span data-stu-id="029e0-112">Serial Number</span></span>

<span data-ttu-id="029e0-113">Contient un entier positif unique attribué au certificat par l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="029e0-113">Contains a positive, unique integer assigned by the certification authority (CA) to the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Certificate serial number
---------------------------------------------------------------------
CertificateSerialNumber ::= INTEGER
```

## <a name="signature-algorithm"></a><span data-ttu-id="029e0-114">Algorithme de signature</span><span class="sxs-lookup"><span data-stu-id="029e0-114">Signature Algorithm</span></span>

<span data-ttu-id="029e0-115">Contient un [*identificateur d’objet*](/windows/desktop/SecGloss/o-gly) (OID) qui spécifie l’algorithme utilisé par l’autorité de certification pour signer le certificat.</span><span class="sxs-lookup"><span data-stu-id="029e0-115">Contains an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) that specifies the algorithm used by the CA to sign the certificate.</span></span> <span data-ttu-id="029e0-116">Par exemple, 1.2.840.113549.1.1.5 indique un algorithme de hachage SHA-1 associé à l’algorithme de chiffrement RSA de RSA Laboratories.</span><span class="sxs-lookup"><span data-stu-id="029e0-116">For example, 1.2.840.113549.1.1.5 specifies a SHA-1 hashing algorithm combined with the RSA encryption algorithm from RSA Laboratories.</span></span>

``` syntax
---------------------------------------------------------------------
-- Signature OID
---------------------------------------------------------------------
signature ::= AlgorithmIdentifier

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="issuer"></a><span data-ttu-id="029e0-117">Émetteur</span><span class="sxs-lookup"><span data-stu-id="029e0-117">Issuer</span></span>

<span data-ttu-id="029e0-118">Contient le nom unique (DN) [*X. 500*](/windows/desktop/SecGloss/x-gly) de l’autorité de certification qui a créé et signé le certificat.</span><span class="sxs-lookup"><span data-stu-id="029e0-118">Contains the [*X.500*](/windows/desktop/SecGloss/x-gly) distinguished name (DN) of the CA that created and signed the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Issuer name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="validity"></a><span data-ttu-id="029e0-119">Validité</span><span class="sxs-lookup"><span data-stu-id="029e0-119">Validity</span></span>

<span data-ttu-id="029e0-120">Indique l’intervalle de temps pendant lequel le certificat est valable.</span><span class="sxs-lookup"><span data-stu-id="029e0-120">Specifies the time interval during which the certificate is valid.</span></span> <span data-ttu-id="029e0-121">Les dates jusqu’à la fin du 2049 utilisent le format de temps universel coordonné (heure de Greenwich) (*YYMMDDHHMMSSZ*).</span><span class="sxs-lookup"><span data-stu-id="029e0-121">Dates through the end of 2049 use the Coordinated Universal Time (Greenwich Mean Time) format (*yymmddhhmmssz*).</span></span> <span data-ttu-id="029e0-122">Les dates commençant au 1er janvier 2050 utilisent le format d’heure généralisée (*yyyymmddhhmmssz*).</span><span class="sxs-lookup"><span data-stu-id="029e0-122">Dates beginning with January 1st, 2050 use the generalized time format (*yyyymmddhhmmssz*).</span></span>

``` syntax
---------------------------------------------------------------------
-- Validity period 
---------------------------------------------------------------------
Validity ::= SEQUENCE 
{
  notBefore           ChoiceOfTime,
  notAfter            ChoiceOfTime
}

ChoiceOfTime ::= CHOICE 
{
  utcTime                 UTCTime,
  generalTime             GeneralizedTime
}
```

## <a name="subject"></a><span data-ttu-id="029e0-123">Objet</span><span class="sxs-lookup"><span data-stu-id="029e0-123">Subject</span></span>

<span data-ttu-id="029e0-124">Contient le nom unique X.500 de l’entité associée à la clé publique incluse dans le certificat.</span><span class="sxs-lookup"><span data-stu-id="029e0-124">Contains an X.500 distinguished name of the entity associated with the public key contained in the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Subject name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="public-key"></a><span data-ttu-id="029e0-125">Clé publique</span><span class="sxs-lookup"><span data-stu-id="029e0-125">Public Key</span></span>

<span data-ttu-id="029e0-126">Contient la clé publique et des informations sur l’algorithme associé.</span><span class="sxs-lookup"><span data-stu-id="029e0-126">Contains the public key and associated algorithm information.</span></span>

``` syntax
---------------------------------------------------------------------
--  Subject public key information
---------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
  algorithm           AlgorithmIdentifier,
  subjectPublicKey    BITSTRING
}

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="related-topics"></a><span data-ttu-id="029e0-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="029e0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="029e0-128">Champs de la version 2</span><span class="sxs-lookup"><span data-stu-id="029e0-128">Version 2 Fields</span></span>](about-version-2-fields.md)
</dt> <dt>

[<span data-ttu-id="029e0-129">Extensions de la version 3</span><span class="sxs-lookup"><span data-stu-id="029e0-129">Version 3 Extensions</span></span>](about-version-3-extensions.md)
</dt> <dt>

[<span data-ttu-id="029e0-130">Certificats de clé publique X. 509</span><span class="sxs-lookup"><span data-stu-id="029e0-130">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 
