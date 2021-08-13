---
description: L’API d’inscription de certificats utilise le format ASN. 1 (Abstract Syntax Notation One) pour définir, encoder et décoder les demandes de certificat et les certificats qu’elle transfère entre les ordinateurs clients et les autorités de certification.
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: Présentation de la syntaxe et de l’encodage ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504f6e643d91951351eaef2c51f9cfeac01919c77718a88ce866670f22803146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904228"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a>Présentation de la syntaxe et de l’encodage ASN. 1

L’API d’inscription de certificats utilise le format ASN. 1 (Abstract Syntax Notation One) pour définir, encoder et décoder les demandes de certificat et les certificats qu’elle transfère entre les ordinateurs clients et les autorités de certification. ASN. 1 peut être divisé de manière conceptuelle en un ensemble de règles syntaxiques et un ensemble de règles d’encodage, comme indiqué dans les exemples suivants.

## <a name="asn1-syntax-example"></a>Exemple de Syntaxe ASN. 1

Une demande de certificat contient, entre autres choses, le nom de l’entité qui effectue la demande ou pour laquelle la demande est effectuée. Le nom est une séquence de noms uniques (RDN) X. 500. Chaque RDN dans la séquence se compose d’un identificateur d’objet (OID) et d’une valeur. La syntaxe ASN. 1 pour un nom de sujet est présentée dans l’exemple suivant.

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

## <a name="asn1-encoding-example"></a>Exemple d’encodage ASN. 1

l’API d’inscription de certificats utilise [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) pour encoder le nom d’objet précédent. DER exige que chaque élément du nom soit représenté par un triplet TLV où T contient le numéro de balise du type ASN. 1, L contient la longueur et V contient la valeur associée. L’exemple suivant montre comment le nom de sujet TestCN. TestOrg est encodé.

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

Notez les points suivants :

-   Ligne 1 :<dl> Le nom est une séquence de noms uniques relatifs.  
    Le numéro de balise pour le type de **séquence** est 0x30.  
    Le nom d’objet de TestCN. TestOrg requiert 35 (0x23) octets.  
    </dl>
-   Line 2:<dl> Le nom commun, TestCN, est un ensemble unique de structures **AttributeTypeValue** .  
    Le numéro de balise d’un **jeu** est 0x31.  
    </dl>
-   Ligne 3 :<dl> La structure **AttributeTypeValue** est une séquence.  
    Le numéro de balise pour le type de **séquence** est 0x30.  
    La structure requiert 13 (0xD) octets.  
    </dl>
-   Lignes 4 à 6 :<dl> L’identificateur d’objet (OID) pour le nom commun est 2.5.4.3.  
    L’OID est un type d' **\_ ID d’objet** de trois octets.  
    Le numéro de balise pour le type d' **\_ ID d’objet** est 0x06.  
    </dl>
-   Lignes 7 à 9 :<dl> Le nom commun, TestCN, est une valeur de chaîne.  
    La chaîne est un type de **\_ chaîne imprimable** de six octets.  
    Le numéro de balise pour le type de **\_ chaîne imprimable** est 0x13.  
    </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Système de type ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Encodage de demande de certificat](about-certificate-request-encoding.md)
</dt> <dt>

[Codage DER des types ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 
