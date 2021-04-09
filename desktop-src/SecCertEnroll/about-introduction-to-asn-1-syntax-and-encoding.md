---
description: L’API d’inscription de certificats utilise le format ASN. 1 (Abstract Syntax Notation One) pour définir, encoder et décoder les demandes de certificat et les certificats qu’elle transfère entre les ordinateurs clients et les autorités de certification.
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: Présentation de la syntaxe et de l’encodage ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4fe15d2fb8fba4af25b9da7c249fec3a92630e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865030"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a><span data-ttu-id="4ac5a-103">Présentation de la syntaxe et de l’encodage ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4ac5a-103">Introduction to ASN.1 Syntax and Encoding</span></span>

<span data-ttu-id="4ac5a-104">L’API d’inscription de certificats utilise le format ASN. 1 (Abstract Syntax Notation One) pour définir, encoder et décoder les demandes de certificat et les certificats qu’elle transfère entre les ordinateurs clients et les autorités de certification.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-104">The Certificate Enrollment API uses Abstract Syntax Notation One (ASN.1) to define, encode, and decode the certificate requests and certificates that it transfers between client computers and certification authorities.</span></span> <span data-ttu-id="4ac5a-105">ASN. 1 peut être divisé de manière conceptuelle en un ensemble de règles syntaxiques et un ensemble de règles d’encodage, comme indiqué dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-105">ASN.1 can be conceptually divided into a set of syntax rules and a set of encoding rules as shown by the following examples.</span></span>

## <a name="asn1-syntax-example"></a><span data-ttu-id="4ac5a-106">Exemple de Syntaxe ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4ac5a-106">ASN.1 Syntax Example</span></span>

<span data-ttu-id="4ac5a-107">Une demande de certificat contient, entre autres choses, le nom de l’entité qui effectue la demande ou pour laquelle la demande est effectuée.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-107">A certificate request contains, among other things, the name of the entity that is making the request or for which the request is being made.</span></span> <span data-ttu-id="4ac5a-108">Le nom est une séquence de noms uniques (RDN) X. 500.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-108">The name is a sequence of X.500 relative distinguished names (RDNs).</span></span> <span data-ttu-id="4ac5a-109">Chaque RDN dans la séquence se compose d’un identificateur d’objet (OID) et d’une valeur.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-109">Each RDN in the sequence consists of an object identifier (OID) and a value.</span></span> <span data-ttu-id="4ac5a-110">La syntaxe ASN. 1 pour un nom de sujet est présentée dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-110">The ASN.1 syntax for a subject name is shown in the following example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Subject name
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}
```

## <a name="asn1-encoding-example"></a><span data-ttu-id="4ac5a-111">Exemple d’encodage ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4ac5a-111">ASN.1 Encoding Example</span></span>

<span data-ttu-id="4ac5a-112">L’API d’inscription de certificats utilise [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) pour encoder le nom d’objet précédent.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-112">The Certificate Enrollment API uses [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) to encode the preceding subject name.</span></span> <span data-ttu-id="4ac5a-113">DER exige que chaque élément du nom soit représenté par un triplet TLV où T contient le numéro de balise du type ASN. 1, L contient la longueur et V contient la valeur associée.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-113">DER requires that each item in the name be represented by a TLV triplet where T contains the tag number of the ASN.1 type, L contains the length, and V contains the associated value.</span></span> <span data-ttu-id="4ac5a-114">L’exemple suivant montre comment le nom de sujet TestCN. TestOrg est encodé.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-114">The following example shows how the subject name TestCN.TestOrg is encoded.</span></span>

``` syntax
1.     30 23            ; SEQUENCE (23 Bytes)
2.     |  |  31 0f            ; SET (f Bytes)
3.     |  |  |  30 0d            ; SEQUENCE (d Bytes)
4.     |  |  |     06 03         ; OBJECT_ID (3 Bytes)
5.     |  |  |     |  55 04 03
6.     |  |  |     |     ; 2.5.4.3 Common Name (CN)
7.     |  |  |     13 06         ; PRINTABLE_STRING (6 Bytes)
8.     |  |  |        54 65 73 74 43 4e                    ; TestCN
9.     |  |  |           ; "TestCN"
10.    |  |  31 10            ; SET (10 Bytes)
11.    |  |     30 0e            ; SEQUENCE (e Bytes)
12.    |  |        06 03         ; OBJECT_ID (3 Bytes)
13.    |  |        |  55 04 0a
14.    |  |        |     ; 2.5.4.10 Organization (O)
15.    |  |        13 07         ; PRINTABLE_STRING (7 Bytes)
16.    |  |           54 65 73 74 4f 72 67                 ; TestOrg
17.    |  |              ; "TestOrg"
```

<span data-ttu-id="4ac5a-115">Notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="4ac5a-115">Note the following points:</span></span>

-   <span data-ttu-id="4ac5a-116">Ligne 1 :</span><span class="sxs-lookup"><span data-stu-id="4ac5a-116">Line 1:</span></span><dl> <span data-ttu-id="4ac5a-117">Le nom est une séquence de noms uniques relatifs.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-117">The name is a sequence of relative distinguished names.</span></span>  
    <span data-ttu-id="4ac5a-118">Le numéro de balise pour le type de **séquence** est 0x30.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-118">The tag number for the **SEQUENCE** type is 0x30.</span></span>  
    <span data-ttu-id="4ac5a-119">Le nom d’objet de TestCN. TestOrg requiert 35 (0x23) octets.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-119">The subject name of TestCN.TestOrg requires 35 (0x23) bytes.</span></span>  
    </dl>
-   Line 2:<dl> <span data-ttu-id="4ac5a-120">Le nom commun, TestCN, est un ensemble unique de structures **AttributeTypeValue** .</span><span class="sxs-lookup"><span data-stu-id="4ac5a-120">The Common Name, TestCN, is a single set of **AttributeTypeValue** structures.</span></span>  
    <span data-ttu-id="4ac5a-121">Le numéro de balise d’un **jeu** est 0x31.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-121">The tag number for a **SET** is 0x31.</span></span>  
    </dl><span data-ttu-id="4ac5a-122">
-   Ligne 3 :</span><span class="sxs-lookup"><span data-stu-id="4ac5a-122">
-   Line 3:</span></span><dl> <span data-ttu-id="4ac5a-123">La structure **AttributeTypeValue** est une séquence.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-123">The **AttributeTypeValue** structure is a sequence.</span></span>  
    <span data-ttu-id="4ac5a-124">Le numéro de balise pour le type de **séquence** est 0x30.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-124">The tag number for the **SEQUENCE** type is 0x30.</span></span>  
    <span data-ttu-id="4ac5a-125">La structure requiert 13 (0xD) octets.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-125">The structure requires 13 (0xD) bytes.</span></span>  
    </dl><span data-ttu-id="4ac5a-126">
-   Lignes 4 à 6 :</span><span class="sxs-lookup"><span data-stu-id="4ac5a-126">
-   Lines 4 to 6:</span></span><dl> <span data-ttu-id="4ac5a-127">L’identificateur d’objet (OID) pour le nom commun est 2.5.4.3.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-127">The object identifier (OID) for the Common Name is 2.5.4.3.</span></span>  
    <span data-ttu-id="4ac5a-128">L’OID est un type d' **\_ ID d’objet** de trois octets.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-128">The OID is a three byte **OBJECT\_ID** type.</span></span>  
    <span data-ttu-id="4ac5a-129">Le numéro de balise pour le type d' **\_ ID d’objet** est 0x06.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-129">The tag number for the **OBJECT\_ID** type is 0x06.</span></span>  
    </dl><span data-ttu-id="4ac5a-130">
-   Lignes 7 à 9 :</span><span class="sxs-lookup"><span data-stu-id="4ac5a-130">
-   Lines 7 to 9:</span></span><dl> <span data-ttu-id="4ac5a-131">Le nom commun, TestCN, est une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-131">The Common Name, TestCN, is a string value.</span></span>  
    <span data-ttu-id="4ac5a-132">La chaîne est un type de **\_ chaîne imprimable** de six octets.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-132">The string is a six byte **PRINTABLE\_STRING** type.</span></span>  
    <span data-ttu-id="4ac5a-133">Le numéro de balise pour le type de **\_ chaîne imprimable** est 0x13.</span><span class="sxs-lookup"><span data-stu-id="4ac5a-133">The tag number for the **PRINTABLE\_STRING** type is 0x13.</span></span>  
    </dl>

## <a name="related-topics"></a><span data-ttu-id="4ac5a-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ac5a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ac5a-135">Système de type ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4ac5a-135">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="4ac5a-136">Encodage de demande de certificat</span><span class="sxs-lookup"><span data-stu-id="4ac5a-136">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="4ac5a-137">Codage DER des types ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4ac5a-137">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="4ac5a-138">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="4ac5a-138">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 
