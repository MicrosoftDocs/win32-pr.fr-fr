---
description: Un type ASN. 1 (Abstract Syntax Notation One) construit est constitué de types de base, de types chaîne ou d’autres types construits. Par exemple, une extension de certificat X. 509 est composée de trois types ASN. 1 de base, comme indiqué dans l’exemple suivant.
ms.assetid: 90c52d71-5d5b-479c-8e29-06c9f0f6da4a
title: Types construits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a515e6e03ebf3c95ff1cabc1bf7f12eb423df27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514413"
---
# <a name="constructed-types"></a><span data-ttu-id="6ed8e-104">Types construits</span><span class="sxs-lookup"><span data-stu-id="6ed8e-104">Constructed Types</span></span>

<span data-ttu-id="6ed8e-105">Un type ASN. 1 ( [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) ) construit est constitué de types de base, de types chaîne ou d’autres types construits.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-105">A constructed [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) type is made up from basic types, string types, or other constructed types.</span></span> <span data-ttu-id="6ed8e-106">Par exemple, une extension de certificat X. 509 est composée de trois types ASN. 1 de base, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-106">For example, an X.509 certificate extension is composed from three basic ASN.1 types as shown by the following example.</span></span>

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

<span data-ttu-id="6ed8e-107">Une extension se compose d’un [*identificateur d’objet*](/windows/desktop/SecGloss/o-gly) (OID), d’une valeur booléenne qui identifie si l’extension est essentielle et d’un tableau d’octets qui contient la valeur.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-107">An extension consists of an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID), a Boolean value that identifies whether the extension is critical, and a byte array that contains the value.</span></span> <span data-ttu-id="6ed8e-108">L’API d’inscription de certificats prend en charge les types ASN. 1 construits suivants.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-108">The Certificate Enrollment API supports the following constructed ASN.1 types.</span></span>

## <a name="sequence-and-sequence-of"></a><span data-ttu-id="6ed8e-109">SÉQUENCE et séquence de</span><span class="sxs-lookup"><span data-stu-id="6ed8e-109">SEQUENCE and SEQUENCE OF</span></span>

<span data-ttu-id="6ed8e-110">Balise d’encodage : 0x30</span><span class="sxs-lookup"><span data-stu-id="6ed8e-110">Encoding tag: 0x30</span></span>

<span data-ttu-id="6ed8e-111">Contient une série ordonnée de champs d’un ou plusieurs types.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-111">Contains an ordered series of fields of one or more types.</span></span> <span data-ttu-id="6ed8e-112">Les champs peuvent être marqués comme **facultatifs** ou **par défaut**.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-112">Fields can be marked **OPTIONAL** or **DEFAULT**.</span></span> <span data-ttu-id="6ed8e-113">En outre, pour éviter toute ambiguïté lors du décodage, les champs facultatifs successifs doivent différer les uns des autres à l’aide d’un identificateur unique (un entier entre crochets comme \[ 1 \] ) et d’un champ obligatoire suivant, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-113">Also, to avoid ambiguity when decoding, successive optional fields should differ from one another by use of a unique identifier (a bracketed integer such as \[1\]) and from a following required field as shown by the following example.</span></span>

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

<span data-ttu-id="6ed8e-114">La différence entre la **séquence** et la **séquence de** est que les éléments d’une **séquence de** construction doivent être du même type.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-114">The difference between **SEQUENCE** and **SEQUENCE OF** is that the elements of a **SEQUENCE OF** construct must be of the same type.</span></span> <span data-ttu-id="6ed8e-115">Consultez l’exemple qui suit.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-115">See the following example.</span></span> <span data-ttu-id="6ed8e-116">Les deux constructions ont la même valeur de balise (0x30) lors de l’encodage.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-116">Both constructs have the same tag value (0x30) when encoded.</span></span>

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

<span data-ttu-id="6ed8e-117">Une autre façon d’examiner la différence entre la **séquence** et la **séquence de** est de les comparer à leurs équivalents dans le langage de programmation C.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-117">Another way to look at the difference between **SEQUENCE** and **SEQUENCE OF** is to compare them to their counterparts in the C programming language.</span></span> <span data-ttu-id="6ed8e-118">Autrement dit, la **séquence** est à peu près équivalente à une structure et une **séquence de** est à peu près équivalente à un tableau.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-118">That is, **SEQUENCE** is roughly equivalent to a structure and **SEQUENCE OF** is roughly equivalent to an array.</span></span>

## <a name="set-and-set-of"></a><span data-ttu-id="6ed8e-119">SET et SET de</span><span class="sxs-lookup"><span data-stu-id="6ed8e-119">SET and SET OF</span></span>

<span data-ttu-id="6ed8e-120">Balise d’encodage : 0x31</span><span class="sxs-lookup"><span data-stu-id="6ed8e-120">Encoding tag: 0x31</span></span>

<span data-ttu-id="6ed8e-121">Contient une série non triée de champs d’un ou de plusieurs types.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-121">Contains an unordered series of fields of one or more types.</span></span> <span data-ttu-id="6ed8e-122">Cela diffère d’une **séquence** qui contient une liste triée.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-122">This differs from a **SEQUENCE** which contains an ordered list.</span></span> <span data-ttu-id="6ed8e-123">La spécification d’une liste non triée permet à une application de fournir les champs de structure à l’encodeur dans l’ordre le plus approprié.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-123">Specifying an unordered list enables an application to provide the structure fields to the encoder in the most appropriate order.</span></span> <span data-ttu-id="6ed8e-124">Comme pour la **séquence**, les champs d’une construction **Set** peuvent être marqués avec **Optional** ou **default**, et les identificateurs uniques doivent être utilisés pour lever toute ambiguïté au niveau du processus de décodage.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-124">As with **SEQUENCE**, the fields of a **SET** construct can be marked with **OPTIONAL** or **DEFAULT**, and unique identifiers must be used to disambiguate the decoding process.</span></span> <span data-ttu-id="6ed8e-125">La différence entre **Set** et **set de** est que les éléments d’un **ensemble de** constructions doivent être du même type.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-125">The difference between **SET** and **SET OF** is that the elements of a **SET OF** construct must be of the same type.</span></span>

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a><span data-ttu-id="6ed8e-126">SÉLECTIONNÉE</span><span class="sxs-lookup"><span data-stu-id="6ed8e-126">CHOICE</span></span>

<span data-ttu-id="6ed8e-127">Balise d’encodage : non applicable</span><span class="sxs-lookup"><span data-stu-id="6ed8e-127">Encoding tag: not applicable</span></span>

<span data-ttu-id="6ed8e-128">Définit le choix entre les alternatives.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-128">Defines a choice between alternatives.</span></span> <span data-ttu-id="6ed8e-129">Chaque alternative doit être identifiée de manière unique par un entier entre crochets afin d’éviter toute ambiguïté lors du décodage.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-129">Each alternative must be uniquely identified by a bracketed integer to avoid ambiguity when decoding.</span></span> <span data-ttu-id="6ed8e-130">Lorsqu’elle est encodée, la construction **Choice** aura la valeur Tag d’encodage de l’alternative choisie.</span><span class="sxs-lookup"><span data-stu-id="6ed8e-130">When encoded, the **CHOICE** construct will have the encoding tag value of the chosen alternative.</span></span>

``` syntax
AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SeqOfAny,
   directoryName           [4] EXPLICIT Name,
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}
```

## <a name="related-topics"></a><span data-ttu-id="6ed8e-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ed8e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ed8e-132">Système de type ASN. 1</span><span class="sxs-lookup"><span data-stu-id="6ed8e-132">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="6ed8e-133">Codage DER des types ASN. 1</span><span class="sxs-lookup"><span data-stu-id="6ed8e-133">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="6ed8e-134">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="6ed8e-134">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 
