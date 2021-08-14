---
description: L’API d’inscription de certificats prend en charge les types ASN. 1 de base suivants.
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: Types de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e2cc1b8825872789d095616e868fe39e306736583f8ea1784543808b7ec4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905044"
---
# <a name="basic-types"></a>Types de base

L’API d’inscription de certificats prend en charge les types ASN. 1 de base suivants.

## <a name="bit-string"></a>CHAÎNE DE BITS

Balise d’encodage : 0x03

Nom de la Certreq.exe : chaîne de bits \_

Une chaîne binaire ou binaire est un tableau arbitrairement long de bits. Des bits spécifiques peuvent être identifiés par des entiers entre parenthèses et des noms affectés, comme dans l’exemple suivant.

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

Les clés de certificat et les signatures sont souvent représentées sous forme de chaînes binaires.

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

## <a name="boolean"></a>BOOLEAN

Balise d’encodage : 0x01

Nom du Certreq.exe : booléen

Un type booléen peut contenir l’une des deux valeurs suivantes : **true** ou **false**. L’exemple suivant illustre la structure ASN. 1 pour une extension de certificat de contraintes de base. Le champ **autorité de certification** spécifie si un sujet de certificat est une autorité de certification (ca). L’importance par défaut est **false**.

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

## <a name="integer"></a>INTEGER

Balise d’encodage : 0x02

Nom de la Certreq.exe : entier

Un entier peut généralement être une valeur intégrale positive ou négative. L’exemple suivant illustre la structure ASN. 1 pour une clé publique RSA. Notez que le champ **publicExponent** est limité à un entier positif inférieur à 4 294 967 296.

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

## <a name="null"></a>NULL

Balise d’encodage : 0x05

Nom de la Certreq.exe : **null**

Un type **null** contient un seul octet 0x00. Elle peut être utilisée partout où la demande de certificat doit indiquer une valeur vide. Par exemple, un **AlgorithmIdentifier** est une séquence qui contient un identificateur d’objet (OID) et des paramètres facultatifs.

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

En l’absence de paramètres lors de l’encodage de la structure, la valeur **null** est utilisée pour indiquer une valeur vide.

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a>IDENTIFICATEUR D’OBJET

Balise d’encodage : 0x06

Nom de l' Certreq.exe : ID de l’objet \_

L’API d’inscription de certificats utilise des identificateurs d’objet (OID) comme type de pointeur universel pour les identificateurs d’algorithme, les attributs et d’autres éléments de l’infrastructure à clé publique. Les OID sont généralement présentés dans une chaîne décimale séparée par des points, par exemple « 2.16.840.1.101.3.4.1.42 ». Les éléments individuels de la chaîne, séparés par des points, représentent les arcs et les feuilles dans une arborescence d’autorité d’inscription qui identifie de façon unique l’objet et l’organisation qui l’a inscrit. Par exemple, l’OID précédent peut être étendu à l’Organisation conjointe ISO-ITU-t (2) pays (16) États-Unis (840) (1) gov (101) csor (3) nistAlgorithms (4) aesAlgs (1) avec. 42 ajouté pour identifier de manière unique l’algorithme en mode CBC (chiffrement de blocs) AES 256 bits.

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

## <a name="octet-string"></a>CHAÎNE D’OCTETS

Balise d’encodage : 0x04

Nom de la Certreq.exe : chaîne d’octets \_

Une chaîne d’octets est un tableau d’octets arbitrairement volumineux. Contrairement au type de **chaîne de bits** , toutefois, les noms et octets spécifiques de la chaîne ne peuvent pas être attribués à des noms. Le mot octet est conçu pour être indépendant de la plateforme pour faire référence à un mot mémoire. Dans le contexte de l’API d’inscription de certificats, octet et octet sont interchangeables.

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

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Système de type ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Codage DER des types ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



