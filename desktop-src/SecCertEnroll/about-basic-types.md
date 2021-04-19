---
description: L’API d’inscription de certificats prend en charge les types ASN. 1 de base suivants.
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: Types de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f3ae64c058fce3466ca06e7bf205c4c4165fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519698"
---
# <a name="basic-types"></a><span data-ttu-id="39a15-103">Types de base</span><span class="sxs-lookup"><span data-stu-id="39a15-103">Basic Types</span></span>

<span data-ttu-id="39a15-104">L’API d’inscription de certificats prend en charge les types ASN. 1 de base suivants.</span><span class="sxs-lookup"><span data-stu-id="39a15-104">The Certificate Enrollment API supports the following basic ASN.1 types.</span></span>

## <a name="bit-string"></a><span data-ttu-id="39a15-105">CHAÎNE DE BITS</span><span class="sxs-lookup"><span data-stu-id="39a15-105">BIT STRING</span></span>

<span data-ttu-id="39a15-106">Balise d’encodage : 0x03</span><span class="sxs-lookup"><span data-stu-id="39a15-106">Encoding tag: 0x03</span></span>

<span data-ttu-id="39a15-107">Nom de la Certreq.exe : chaîne de bits \_</span><span class="sxs-lookup"><span data-stu-id="39a15-107">Certreq.exe name: BIT\_STRING</span></span>

<span data-ttu-id="39a15-108">Une chaîne binaire ou binaire est un tableau arbitrairement long de bits.</span><span class="sxs-lookup"><span data-stu-id="39a15-108">A bit or binary string is an arbitrarily long array of bits.</span></span> <span data-ttu-id="39a15-109">Des bits spécifiques peuvent être identifiés par des entiers entre parenthèses et des noms affectés, comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="39a15-109">Specific bits can be identified by parenthesized integers and assigned names as in the following example.</span></span>

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

<span data-ttu-id="39a15-110">Les clés de certificat et les signatures sont souvent représentées sous forme de chaînes binaires.</span><span class="sxs-lookup"><span data-stu-id="39a15-110">Certificate keys and signatures are often represented as bit strings.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BIT STRING
-- Tag number: 0x03
---------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
  algorithm           AlgorithmIdentifier,
  subjectPublicKey    BIT STRING
} 
```

## <a name="boolean"></a><span data-ttu-id="39a15-111">BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="39a15-111">BOOLEAN</span></span>

<span data-ttu-id="39a15-112">Balise d’encodage : 0x01</span><span class="sxs-lookup"><span data-stu-id="39a15-112">Encoding tag: 0x01</span></span>

<span data-ttu-id="39a15-113">Nom du Certreq.exe : booléen</span><span class="sxs-lookup"><span data-stu-id="39a15-113">Certreq.exe name: BOOLEAN</span></span>

<span data-ttu-id="39a15-114">Un type booléen peut contenir l’une des deux valeurs suivantes : **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="39a15-114">A Boolean type can contain one of two values, **TRUE** or **FALSE**.</span></span> <span data-ttu-id="39a15-115">L’exemple suivant illustre la structure ASN. 1 pour une extension de certificat de contraintes de base.</span><span class="sxs-lookup"><span data-stu-id="39a15-115">The following example shows the ASN.1 structure for a Basic Constraints certificate extension.</span></span> <span data-ttu-id="39a15-116">Le champ **autorité de certification** spécifie si un sujet de certificat est une autorité de certification (ca).</span><span class="sxs-lookup"><span data-stu-id="39a15-116">The **cA** field specifies whether a certificate subject is a certification authority (CA).</span></span> <span data-ttu-id="39a15-117">L’importance par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="39a15-117">The default criticality is **FALSE**.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BOOLEAN
-- Tag number: 0x01
---------------------------------------------------------------------
BasicConstraints ::= SEQUENCE 
{
  cA                  BOOLEAN DEFAULT FALSE,
  pathLenConstraint   INTEGER OPTIONAL
}
```

## <a name="integer"></a><span data-ttu-id="39a15-118">INTEGER</span><span class="sxs-lookup"><span data-stu-id="39a15-118">INTEGER</span></span>

<span data-ttu-id="39a15-119">Balise d’encodage : 0x02</span><span class="sxs-lookup"><span data-stu-id="39a15-119">Encoding tag: 0x02</span></span>

<span data-ttu-id="39a15-120">Nom de la Certreq.exe : entier</span><span class="sxs-lookup"><span data-stu-id="39a15-120">Certreq.exe name: INTEGER</span></span>

<span data-ttu-id="39a15-121">Un entier peut généralement être une valeur intégrale positive ou négative.</span><span class="sxs-lookup"><span data-stu-id="39a15-121">An integer can typically be any positive or negative integral value.</span></span> <span data-ttu-id="39a15-122">L’exemple suivant illustre la structure ASN. 1 pour une clé publique RSA.</span><span class="sxs-lookup"><span data-stu-id="39a15-122">The following example shows the ASN.1 structure for an RSA public key.</span></span> <span data-ttu-id="39a15-123">Notez que le champ **publicExponent** est limité à un entier positif inférieur à 4 294 967 296.</span><span class="sxs-lookup"><span data-stu-id="39a15-123">Note that the **publicExponent** field is restricted to a positive integer less than 4,294,967,296.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: INTEGER
-- Tag number: 0x02
---------------------------------------------------------------------
HUGEINTEGER ::= INTEGER

RSAPublicKey ::= SEQUENCE 
{ 
  modulus         HUGEINTEGER,    
  publicExponent  INTEGER (0..4294967295) 
} 
```

## <a name="null"></a><span data-ttu-id="39a15-124">NULL</span><span class="sxs-lookup"><span data-stu-id="39a15-124">NULL</span></span>

<span data-ttu-id="39a15-125">Balise d’encodage : 0x05</span><span class="sxs-lookup"><span data-stu-id="39a15-125">Encoding tag: 0x05</span></span>

<span data-ttu-id="39a15-126">Nom de la Certreq.exe : **null**</span><span class="sxs-lookup"><span data-stu-id="39a15-126">Certreq.exe name: **NULL**</span></span>

<span data-ttu-id="39a15-127">Un type **null** contient un seul octet 0x00.</span><span class="sxs-lookup"><span data-stu-id="39a15-127">A **NULL** type contains a single byte 0x00.</span></span> <span data-ttu-id="39a15-128">Elle peut être utilisée partout où la demande de certificat doit indiquer une valeur vide.</span><span class="sxs-lookup"><span data-stu-id="39a15-128">It can be used anywhere that the certificate request must indicate an empty value.</span></span> <span data-ttu-id="39a15-129">Par exemple, un **AlgorithmIdentifier** est une séquence qui contient un identificateur d’objet (OID) et des paramètres facultatifs.</span><span class="sxs-lookup"><span data-stu-id="39a15-129">For example, an **AlgorithmIdentifier** is a sequence that contains an object identifier (OID) and optional parameters.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: NULL
-- Tag number: 0x05
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

<span data-ttu-id="39a15-130">En l’absence de paramètres lors de l’encodage de la structure, la valeur **null** est utilisée pour indiquer une valeur vide.</span><span class="sxs-lookup"><span data-stu-id="39a15-130">If there are no parameters when the structure is encoded, **NULL** is used to indicate an empty value.</span></span>

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a><span data-ttu-id="39a15-131">IDENTIFICATEUR D’OBJET</span><span class="sxs-lookup"><span data-stu-id="39a15-131">OBJECT IDENTIFIER</span></span>

<span data-ttu-id="39a15-132">Balise d’encodage : 0x06</span><span class="sxs-lookup"><span data-stu-id="39a15-132">Encoding tag: 0x06</span></span>

<span data-ttu-id="39a15-133">Nom de l' Certreq.exe : ID de l’objet \_</span><span class="sxs-lookup"><span data-stu-id="39a15-133">Certreq.exe name: OBJECT\_ID</span></span>

<span data-ttu-id="39a15-134">L’API d’inscription de certificats utilise des identificateurs d’objet (OID) comme type de pointeur universel pour les identificateurs d’algorithme, les attributs et d’autres éléments de l’infrastructure à clé publique.</span><span class="sxs-lookup"><span data-stu-id="39a15-134">The Certificate Enrollment API uses object identifiers (OIDs) as a type of universal pointer to algorithm identifiers, attributes, and other PKI elements.</span></span> <span data-ttu-id="39a15-135">Les OID sont généralement présentés dans une chaîne décimale séparée par des points, par exemple « 2.16.840.1.101.3.4.1.42 ».</span><span class="sxs-lookup"><span data-stu-id="39a15-135">OIDs are typically presented in a dotted decimal string such as "2.16.840.1.101.3.4.1.42".</span></span> <span data-ttu-id="39a15-136">Les éléments individuels de la chaîne, séparés par des points, représentent les arcs et les feuilles dans une arborescence d’autorité d’inscription qui identifie de façon unique l’objet et l’organisation qui l’a inscrit.</span><span class="sxs-lookup"><span data-stu-id="39a15-136">The individual elements in the string, separated by periods, represent the arcs and leaves in a registration authority tree that uniquely identifies the object and the organization that registered it.</span></span> <span data-ttu-id="39a15-137">Par exemple, l’OID précédent peut être étendu à l’Organisation conjointe ISO-ITU-t (2) pays (16) États-Unis (840) (1) gov (101) csor (3) nistAlgorithms (4) aesAlgs (1) avec. 42 ajouté pour identifier de manière unique l’algorithme en mode CBC (chiffrement de blocs) AES 256 bits.</span><span class="sxs-lookup"><span data-stu-id="39a15-137">For example, the preceding OID can be expanded to joint-iso-itu-t(2) country(16) us(840) organization(1) gov(101) csor(3) nistAlgorithms(4) aesAlgs(1) with .42 appended to uniquely identify the 256-bit AES cipher block chaining (CBC) mode algorithm.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OBJECT IDENTIFIER
-- Tag number: 0x06
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="octet-string"></a><span data-ttu-id="39a15-138">CHAÎNE D’OCTETS</span><span class="sxs-lookup"><span data-stu-id="39a15-138">OCTET STRING</span></span>

<span data-ttu-id="39a15-139">Balise d’encodage : 0x04</span><span class="sxs-lookup"><span data-stu-id="39a15-139">Encoding tag: 0x04</span></span>

<span data-ttu-id="39a15-140">Nom de la Certreq.exe : chaîne d’octets \_</span><span class="sxs-lookup"><span data-stu-id="39a15-140">Certreq.exe name: OCTET\_STRING</span></span>

<span data-ttu-id="39a15-141">Une chaîne d’octets est un tableau d’octets arbitrairement volumineux.</span><span class="sxs-lookup"><span data-stu-id="39a15-141">An octet string is an arbitrarily large byte array.</span></span> <span data-ttu-id="39a15-142">Contrairement au type de **chaîne de bits** , toutefois, les noms et octets spécifiques de la chaîne ne peuvent pas être attribués à des noms.</span><span class="sxs-lookup"><span data-stu-id="39a15-142">Unlike the **BIT STRING** type, however, specific bits and bytes in the string cannot be assigned names.</span></span> <span data-ttu-id="39a15-143">Le mot octet est conçu pour être indépendant de la plateforme pour faire référence à un mot mémoire.</span><span class="sxs-lookup"><span data-stu-id="39a15-143">The word octet is meant to be a platform independent way to refer to a memory word.</span></span> <span data-ttu-id="39a15-144">Dans le contexte de l’API d’inscription de certificats, octet et octet sont interchangeables.</span><span class="sxs-lookup"><span data-stu-id="39a15-144">Within the context of the Certificate Enrollment API, octet and byte are interchangeable.</span></span>

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OCTET STRING
-- Tag number: 0x04
---------------------------------------------------------------------
AuthorityKeyId ::= SEQUENCE 
{
  keyIdentifier       [0] IMPLICIT OCTET STRING OPTIONAL,
  certIssuer          [1] EXPLICIT NAME
  certSerialNumber    [2] IMPLICIT INTEGER OPTIONAL
}
```

## <a name="related-topics"></a><span data-ttu-id="39a15-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39a15-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39a15-146">Système de type ASN. 1</span><span class="sxs-lookup"><span data-stu-id="39a15-146">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="39a15-147">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="39a15-147">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="39a15-148">Codage DER des types ASN. 1</span><span class="sxs-lookup"><span data-stu-id="39a15-148">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



