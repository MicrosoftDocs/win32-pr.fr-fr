---
description: Le concept de type de données est fondamental pour la norme ASN. 1 (Abstract Syntax Notation One).
ms.assetid: 85e88e0b-057b-42c7-a3c8-017a30195d1e
title: Système de type ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abbf60bf61e32c5fca882f2e40c946c043ef93e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523056"
---
# <a name="asn1-type-system"></a>Système de type ASN. 1

Le concept de type de données est fondamental pour la norme ASN. 1 (Abstract Syntax Notation One). Chaque champ d’une structure de demande de certificat est associé à un type. Considérons, par exemple, la \# syntaxe de certificat PKCS 10 ASN. 1 indiquée dans l’exemple suivant.

``` syntax
--------------------------------------------------------------------
-- PKCS #10 Certificate request.
--------------------------------------------------------------------
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

--------------------------------------------------------------------
-- Version number.
--------------------------------------------------------------------
CertificationRequestInfoVersion ::= INTEGER

--------------------------------------------------------------------
-- Subject distinguished name (DN).
--------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}

--------------------------------------------------------------------
-- Public key information.
--------------------------------------------------------------------
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

--------------------------------------------------------------------
-- Attributes.
--------------------------------------------------------------------
Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   values             AttributeSetValue
}

AttributeSetValue ::= SET OF ANY
```

La structure de requête de haut niveau, **CertificationRequestInfo**, est un type qui est constitué d’une séquence d’autres types. Lorsqu’un type est ou contient uniquement des types de base, des types de chaînes ou **un de ces** types, il ne peut pas être décomposé. Par exemple, le champ **version** est un type **CertificationRequestInfoVersion** qui est, à son tour, un type **entier** , un type ASN. 1 de base qui n’est pas composé d’autres types.

Un système de type permet à la syntaxe d’une demande d’être présentée visuellement de manière compréhensible par les développeurs, et elle permet à la requête d’être encodée de manière cohérente pour la transmission sur un réseau. Pour plus d’informations sur l’encodage, consultez [Distinguished Encoding Rules](distinguished-encoding-rules.md). Pour plus d’informations sur les types ASN. 1, consultez les rubriques suivantes.

[Types de base](about-basic-types.md)

Présente les types de données suivants :

* **CHAÎNE DE BITS**
* **EXPRESSION**
* **INTEGER**
* **NULL**
* **IDENTIFICATEUR D’OBJET**
* **CHAÎNE D’OCTETS**

[Types chaîne](about-string-types.md)

Présente les types de chaînes suivants :

* **BMPString**
* **IA5String**
* **PrintableString**
* **TeletexString**
* **UTF8String**

[Types construits](about-constructed-types.md)

Présente les types de données ASN. 1 qui peuvent contenir des types de base, des types de chaînes ou d’autres types construits.




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Encodage de demande de certificat](about-certificate-request-encoding.md)
</dt> <dt>

[Codage DER des types ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Présentation de la syntaxe et de l’encodage ASN. 1](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



