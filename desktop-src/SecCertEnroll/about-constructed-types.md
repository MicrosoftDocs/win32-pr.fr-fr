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
# <a name="constructed-types"></a>Types construits

Un type ASN. 1 ( [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) ) construit est constitué de types de base, de types chaîne ou d’autres types construits. Par exemple, une extension de certificat X. 509 est composée de trois types ASN. 1 de base, comme indiqué dans l’exemple suivant.

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

Une extension se compose d’un [*identificateur d’objet*](/windows/desktop/SecGloss/o-gly) (OID), d’une valeur booléenne qui identifie si l’extension est essentielle et d’un tableau d’octets qui contient la valeur. L’API d’inscription de certificats prend en charge les types ASN. 1 construits suivants.

## <a name="sequence-and-sequence-of"></a>SÉQUENCE et séquence de

Balise d’encodage : 0x30

Contient une série ordonnée de champs d’un ou plusieurs types. Les champs peuvent être marqués comme **facultatifs** ou **par défaut**. En outre, pour éviter toute ambiguïté lors du décodage, les champs facultatifs successifs doivent différer les uns des autres à l’aide d’un identificateur unique (un entier entre crochets comme \[ 1 \] ) et d’un champ obligatoire suivant, comme indiqué dans l’exemple suivant.

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

La différence entre la **séquence** et la **séquence de** est que les éléments d’une **séquence de** construction doivent être du même type. Consultez l’exemple qui suit. Les deux constructions ont la même valeur de balise (0x30) lors de l’encodage.

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

Une autre façon d’examiner la différence entre la **séquence** et la **séquence de** est de les comparer à leurs équivalents dans le langage de programmation C. Autrement dit, la **séquence** est à peu près équivalente à une structure et une **séquence de** est à peu près équivalente à un tableau.

## <a name="set-and-set-of"></a>SET et SET de

Balise d’encodage : 0x31

Contient une série non triée de champs d’un ou de plusieurs types. Cela diffère d’une **séquence** qui contient une liste triée. La spécification d’une liste non triée permet à une application de fournir les champs de structure à l’encodeur dans l’ordre le plus approprié. Comme pour la **séquence**, les champs d’une construction **Set** peuvent être marqués avec **Optional** ou **default**, et les identificateurs uniques doivent être utilisés pour lever toute ambiguïté au niveau du processus de décodage. La différence entre **Set** et **set de** est que les éléments d’un **ensemble de** constructions doivent être du même type.

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a>SÉLECTIONNÉE

Balise d’encodage : non applicable

Définit le choix entre les alternatives. Chaque alternative doit être identifiée de manière unique par un entier entre crochets afin d’éviter toute ambiguïté lors du décodage. Lorsqu’elle est encodée, la construction **Choice** aura la valeur Tag d’encodage de l’alternative choisie.

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

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Système de type ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codage DER des types ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 
