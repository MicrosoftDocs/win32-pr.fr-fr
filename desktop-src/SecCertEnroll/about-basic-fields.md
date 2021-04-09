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
# <a name="basic-fields"></a>Champs de base

Un certificat X. 509 version 1 contient les champs suivants. Les champs de la version 2 sont abordés dans les champs de la [version 2](about-version-2-fields.md). Les champs de la version 3 sont traités dans les extensions de la [version 3](about-version-3-extensions.md).

## <a name="version"></a>Version

Indique le numéro de version du certificat encodé. Actuellement, les valeurs possibles de ce champ sont 0, 1 ou 2, mais cela peut être développé à l’avenir.

``` syntax
---------------------------------------------------------------------
-- Version number. Currently, this can be 0, 1, or 2.
---------------------------------------------------------------------
CertificateVersion ::= INTEGER {v1(0), v2(1), v3(2)}
```

## <a name="serial-number"></a>Numéro de série

Contient un entier positif unique attribué au certificat par l’autorité de certification.

``` syntax
---------------------------------------------------------------------
-- Certificate serial number
---------------------------------------------------------------------
CertificateSerialNumber ::= INTEGER
```

## <a name="signature-algorithm"></a>Algorithme de signature

Contient un [*identificateur d’objet*](/windows/desktop/SecGloss/o-gly) (OID) qui spécifie l’algorithme utilisé par l’autorité de certification pour signer le certificat. Par exemple, 1.2.840.113549.1.1.5 indique un algorithme de hachage SHA-1 associé à l’algorithme de chiffrement RSA de RSA Laboratories.

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

## <a name="issuer"></a>Émetteur

Contient le nom unique (DN) [*X. 500*](/windows/desktop/SecGloss/x-gly) de l’autorité de certification qui a créé et signé le certificat.

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

## <a name="validity"></a>Validité

Indique l’intervalle de temps pendant lequel le certificat est valable. Les dates jusqu’à la fin du 2049 utilisent le format de temps universel coordonné (heure de Greenwich) (*YYMMDDHHMMSSZ*). Les dates commençant au 1er janvier 2050 utilisent le format d’heure généralisée (*yyyymmddhhmmssz*).

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

## <a name="subject"></a>Objet

Contient le nom unique X.500 de l’entité associée à la clé publique incluse dans le certificat.

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

## <a name="public-key"></a>Clé publique

Contient la clé publique et des informations sur l’algorithme associé.

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

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Champs de la version 2](about-version-2-fields.md)
</dt> <dt>

[Extensions de la version 3](about-version-3-extensions.md)
</dt> <dt>

[Certificats de clé publique X. 509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 
