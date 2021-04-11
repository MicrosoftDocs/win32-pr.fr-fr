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
# <a name="string-types"></a>Types chaîne

L’une des utilisations les plus courantes des chaînes dans une infrastructure à clé publique (PKI) consiste à créer un nom unique X. 500. Par exemple, le nom d’objet d’une demande de certificat est créé en combinant une séquence de noms uniques relatifs, comme indiqué dans l’exemple de syntaxe suivant.

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

L’API d’inscription de certificats prend en charge les types de chaînes ASN. 1 suivants.

## <a name="bmpstring"></a>BMPString

Balise d’encodage : 0x1E

Nom de la Certreq.exe : \_ chaîne Unicode

Le BMP (Basic Multilingual Plane) est un encodage de caractères qui englobe le premier plan du jeu de caractères universels (UCS). Il y a dix-sept plans numérotés de 0 à 16. BMP occupe le plan 0 et comprend des points de code 65 536 compris entre 0x0000 et 0xFFFF. Il s’agit de la section de la table de caractères Unicode dans laquelle la plupart des assignations de caractères ont été effectuées jusqu’à présent. Il comprend le latin, le Moyen-Orient, l’Asie, l’Afrique et d’autres langues.

## <a name="ia5string"></a>IA5String

Balise d’encodage : 0x16

Nom de la Certreq.exe : \_ chaîne IA5

L’alphabet international numéro 5 (IA5) est généralement équivalent à l’alphabet ASCII, mais les différentes versions peuvent inclure des accents ou d’autres caractères spécifiques à une langue régionale. L’exemple suivant montre le type **IA5String** utilisé dans la définition ASN. 1 de l’extension de certificat **AlternativeNames** .

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

## <a name="printablestring"></a>PrintableString

Balise d’encodage : 0x13

Nom de la Certreq.exe : \_ chaîne imprimable

Le type de données **printableString** était à l’origine destiné à représenter les jeux de caractères limités disponibles pour les terminaux d’entrée mainframe, mais il est toujours couramment utilisé. Il contient les caractères suivants :

-   A-Z
-   a-z
-   0-9
-   ' ( ) + , - . / : = ? \[space\]

## <a name="teletexstring"></a>TeletexString

Balise d’encodage : 0x14

Les types de données **teletexString** et **T61String** associés sont encodés sur 8 bits (ou 16 bits pour les caractères composites). Ils ont tous les deux un numéro de balise 0x14. Elles ne sont pas utilisées de manière intensive.

## <a name="utf8string"></a>UTF8String

Balise d’encodage : 0x0C

Nom de la Certreq.exe : \_ chaîne UTF8

Le format UTF-8 de 8 bits est un encodage de caractères de longueur variable qui peut représenter n’importe quel caractère universel sous la forme d’un caractère Unicode tout en permettant aux points de code initiaux de rester cohérents avec ASCII. UTF-8 utilise un à quatre octets. Le numéro de balise est 0x0C.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Système de type ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Codage DER des types ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



