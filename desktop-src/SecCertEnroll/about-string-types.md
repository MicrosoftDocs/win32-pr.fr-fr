---
description: L’une des utilisations les plus courantes des chaînes dans une infrastructure à clé publique (PKI) consiste à créer un nom unique X. 500.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Types chaîne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1173de3b2c4c5fd64181cd19c69cfbcecb1d584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202838"
---
# <a name="string-types"></a><span data-ttu-id="8c57a-103">Types chaîne</span><span class="sxs-lookup"><span data-stu-id="8c57a-103">String Types</span></span>

<span data-ttu-id="8c57a-104">L’une des utilisations les plus courantes des chaînes dans une infrastructure à clé publique (PKI) consiste à créer un nom unique X. 500.</span><span class="sxs-lookup"><span data-stu-id="8c57a-104">One of the most common uses of strings in a public key infrastructure (PKI) is to create an X.500 Distinguished Name.</span></span> <span data-ttu-id="8c57a-105">Par exemple, le nom d’objet d’une demande de certificat est créé en combinant une séquence de noms uniques relatifs, comme indiqué dans l’exemple de syntaxe suivant.</span><span class="sxs-lookup"><span data-stu-id="8c57a-105">For example, the subject name of a certificate request is created by combining a sequence of relative distinguished names as shown in the following syntax example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Breakdown of a subject name in a certificate request.
---------------------------------------------------------------------

CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

<span data-ttu-id="8c57a-106">L’API d’inscription de certificats prend en charge les types de chaînes ASN. 1 suivants.</span><span class="sxs-lookup"><span data-stu-id="8c57a-106">The Certificate Enrollment API supports the following ASN.1 string types.</span></span>

## <a name="bmpstring"></a><span data-ttu-id="8c57a-107">BMPString</span><span class="sxs-lookup"><span data-stu-id="8c57a-107">BMPString</span></span>

<span data-ttu-id="8c57a-108">Balise d’encodage : 0x1E</span><span class="sxs-lookup"><span data-stu-id="8c57a-108">Encoding tag: 0x1E</span></span>

<span data-ttu-id="8c57a-109">Nom de la Certreq.exe : \_ chaîne Unicode</span><span class="sxs-lookup"><span data-stu-id="8c57a-109">Certreq.exe name: UNICODE\_STRING</span></span>

<span data-ttu-id="8c57a-110">Le BMP (Basic Multilingual Plane) est un encodage de caractères qui englobe le premier plan du jeu de caractères universels (UCS).</span><span class="sxs-lookup"><span data-stu-id="8c57a-110">The Basic Multilingual Plane (BMP) is a character encoding that encompasses the first plane of the Universal Character Set (UCS).</span></span> <span data-ttu-id="8c57a-111">Il y a dix-sept plans numérotés de 0 à 16.</span><span class="sxs-lookup"><span data-stu-id="8c57a-111">There are seventeen planes numbered 0 to 16.</span></span> <span data-ttu-id="8c57a-112">BMP occupe le plan 0 et comprend des points de code 65 536 compris entre 0x0000 et 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="8c57a-112">BMP occupies plane 0 and includes 65,536 code points from 0x0000 to 0xFFFF.</span></span> <span data-ttu-id="8c57a-113">Il s’agit de la section de la table de caractères Unicode dans laquelle la plupart des assignations de caractères ont été effectuées jusqu’à présent.</span><span class="sxs-lookup"><span data-stu-id="8c57a-113">This is the section of the Unicode character map where most of the characters assignments have so far been made.</span></span> <span data-ttu-id="8c57a-114">Il comprend le latin, le Moyen-Orient, l’Asie, l’Afrique et d’autres langues.</span><span class="sxs-lookup"><span data-stu-id="8c57a-114">It includes Latin, Middle Eastern, Asian, African, and other languages.</span></span>

## <a name="ia5string"></a><span data-ttu-id="8c57a-115">IA5String</span><span class="sxs-lookup"><span data-stu-id="8c57a-115">IA5String</span></span>

<span data-ttu-id="8c57a-116">Balise d’encodage : 0x16</span><span class="sxs-lookup"><span data-stu-id="8c57a-116">Encoding tag: 0x16</span></span>

<span data-ttu-id="8c57a-117">Nom de la Certreq.exe : \_ chaîne IA5</span><span class="sxs-lookup"><span data-stu-id="8c57a-117">Certreq.exe name: IA5\_STRING</span></span>

<span data-ttu-id="8c57a-118">L’alphabet international numéro 5 (IA5) est généralement équivalent à l’alphabet ASCII, mais les différentes versions peuvent inclure des accents ou d’autres caractères spécifiques à une langue régionale.</span><span class="sxs-lookup"><span data-stu-id="8c57a-118">The International Alphabet number 5 (IA5) is generally equivalent to the ASCII alphabet, but different versions can include accents or other characters specific to a regional language.</span></span> <span data-ttu-id="8c57a-119">L’exemple suivant montre le type **IA5String** utilisé dans la définition ASN. 1 de l’extension de certificat **AlternativeNames** .</span><span class="sxs-lookup"><span data-stu-id="8c57a-119">The following example shows the **IA5String** type used in the ASN.1 definition of the **AlternativeNames** certificate extension.</span></span>

``` syntax
---------------------------------------------------------------------
-- AlternativeNames extension
---------------------------------------------------------------------

AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SEQUENCE OF ANY, 
   directoryName           [4] EXPLICIT ANY,    
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}

OtherName ::= SEQUENCE 
{
   type                    OBJECT IDENTIFIER,
   value                   [0] EXPLICIT ANY 
}
```

## <a name="printablestring"></a><span data-ttu-id="8c57a-120">PrintableString</span><span class="sxs-lookup"><span data-stu-id="8c57a-120">PrintableString</span></span>

<span data-ttu-id="8c57a-121">Balise d’encodage : 0x13</span><span class="sxs-lookup"><span data-stu-id="8c57a-121">Encoding tag: 0x13</span></span>

<span data-ttu-id="8c57a-122">Nom de la Certreq.exe : \_ chaîne imprimable</span><span class="sxs-lookup"><span data-stu-id="8c57a-122">Certreq.exe name: PRINTABLE\_STRING</span></span>

<span data-ttu-id="8c57a-123">Le type de données **printableString** était à l’origine destiné à représenter les jeux de caractères limités disponibles pour les terminaux d’entrée mainframe, mais il est toujours couramment utilisé.</span><span class="sxs-lookup"><span data-stu-id="8c57a-123">The **PrintableString** data type was originally intended to represent the limited character sets available to mainframe input terminals, but it is still commonly used.</span></span> <span data-ttu-id="8c57a-124">Il contient les caractères suivants :</span><span class="sxs-lookup"><span data-stu-id="8c57a-124">It contains the following characters:</span></span>

-   <span data-ttu-id="8c57a-125">A-Z</span><span class="sxs-lookup"><span data-stu-id="8c57a-125">A-Z</span></span>
-   <span data-ttu-id="8c57a-126">a-z</span><span class="sxs-lookup"><span data-stu-id="8c57a-126">a-z</span></span>
-   <span data-ttu-id="8c57a-127">0-9</span><span class="sxs-lookup"><span data-stu-id="8c57a-127">0-9</span></span>
-   <span data-ttu-id="8c57a-128">' ( ) + , - .</span><span class="sxs-lookup"><span data-stu-id="8c57a-128">' ( ) + , - .</span></span> <span data-ttu-id="8c57a-129">/ : = ?</span><span class="sxs-lookup"><span data-stu-id="8c57a-129">/ : = ?</span></span> <span data-ttu-id="8c57a-130">\[space\]</span><span class="sxs-lookup"><span data-stu-id="8c57a-130">\[space\]</span></span>

## <a name="teletexstring"></a><span data-ttu-id="8c57a-131">TeletexString</span><span class="sxs-lookup"><span data-stu-id="8c57a-131">TeletexString</span></span>

<span data-ttu-id="8c57a-132">Balise d’encodage : 0x14</span><span class="sxs-lookup"><span data-stu-id="8c57a-132">Encoding tag: 0x14</span></span>

<span data-ttu-id="8c57a-133">Les types de données **teletexString** et **T61String** associés sont encodés sur 8 bits (ou 16 bits pour les caractères composites).</span><span class="sxs-lookup"><span data-stu-id="8c57a-133">The **TeletexString** and the related **T61String** data types are encoded on 8 bits (or 16 bits for composite characters).</span></span> <span data-ttu-id="8c57a-134">Ils ont tous les deux un numéro de balise 0x14.</span><span class="sxs-lookup"><span data-stu-id="8c57a-134">They both have a tag number of 0x14.</span></span> <span data-ttu-id="8c57a-135">Elles ne sont pas utilisées de manière intensive.</span><span class="sxs-lookup"><span data-stu-id="8c57a-135">They are not extensively used.</span></span>

## <a name="utf8string"></a><span data-ttu-id="8c57a-136">UTF8String</span><span class="sxs-lookup"><span data-stu-id="8c57a-136">UTF8String</span></span>

<span data-ttu-id="8c57a-137">Balise d’encodage : 0x0C</span><span class="sxs-lookup"><span data-stu-id="8c57a-137">Encoding tag: 0x0C</span></span>

<span data-ttu-id="8c57a-138">Nom de la Certreq.exe : \_ chaîne UTF8</span><span class="sxs-lookup"><span data-stu-id="8c57a-138">Certreq.exe name: UTF8\_STRING</span></span>

<span data-ttu-id="8c57a-139">Le format UTF-8 de 8 bits est un encodage de caractères de longueur variable qui peut représenter n’importe quel caractère universel sous la forme d’un caractère Unicode tout en permettant aux points de code initiaux de rester cohérents avec ASCII.</span><span class="sxs-lookup"><span data-stu-id="8c57a-139">The 8-bit UCS/Unicode Transformation Format (UTF-8) is a variable-length character encoding that can represent any universal character as a Unicode character while allowing initial code points to remain consistent with ASCII.</span></span> <span data-ttu-id="8c57a-140">UTF-8 utilise un à quatre octets.</span><span class="sxs-lookup"><span data-stu-id="8c57a-140">UTF-8 uses one to four bytes.</span></span> <span data-ttu-id="8c57a-141">Le numéro de balise est 0x0C.</span><span class="sxs-lookup"><span data-stu-id="8c57a-141">The tag number is 0x0C.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c57a-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c57a-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c57a-143">Système de type ASN. 1</span><span class="sxs-lookup"><span data-stu-id="8c57a-143">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="8c57a-144">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="8c57a-144">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="8c57a-145">Codage DER des types ASN. 1</span><span class="sxs-lookup"><span data-stu-id="8c57a-145">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



