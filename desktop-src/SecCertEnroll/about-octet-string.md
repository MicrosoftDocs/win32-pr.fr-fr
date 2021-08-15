---
description: Le type de données de chaîne ASN. 1 OCTET est encodé dans un triplet TLV qui commence par un octet de balise de 0x04.
ms.assetid: 9d07a6c8-a15f-4030-838c-3063e315684f
title: CHAÎNE D’OCTETS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588547e5211efbe6b4b91a8a72f6644de0c7c4dcbacc570f0a1f272e7cc97962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903743"
---
# <a name="octet-string"></a>CHAÎNE D’OCTETS

Le type de données de chaîne ASN. 1 **octet** est encodé dans un triplet TLV qui commence par un octet de **balise** de 0x04. Les types de données de chaîne d' **octets** et de [chaîne de bits](about-bit-string.md) sont très similaires. Ainsi, les deux types sont encodés de manière similaire, sauf que, étant donné que l’octet de fin d’une **chaîne d’octets** ne peut pas avoir de bits inutilisés, aucun octet de début ne doit être ajouté au contenu. L’exemple suivant, adapté de la rubrique [ASN. 1 encodée par CMC](cmc-encoded-asn-1.md) , montre comment le nom d’un modèle de certificat est encodé sous la forme d’un tableau d’octets.

``` syntax
30 17                                 ; SEQUENCE (17 Bytes)
|  06 09                              ; OBJECT_ID (9 Bytes)
|  |  2b 06 01 04 01 82 37 14  02     ;   1.3.6.1.4.1.311.20.2
|  04 0a                              ; OCTET_STRING (a Bytes)
|     1e 08 00 55 00 73 00 65  00 72  ;   ...U.s.e.r
```

Si le tableau d’octets contient moins de 128 octets, le champ de **longueur** de l’tripleon TLV ne requiert qu’un octet pour spécifier la longueur du contenu. Si la valeur est supérieure à 127 octets, le bit 7 du champ de **longueur** est défini sur 1 et les bits 6 à 0 spécifient le nombre d’octets supplémentaires utilisés pour identifier la longueur du contenu. Cela est illustré dans l’exemple suivant où le bit de poids fort du deuxième octet sur la première ligne a la valeur 1 et l’octet indique qu’il y a un octet de **longueur** de fin. Le troisième octet spécifie donc que le contenu a une longueur de 0x80 octets.

``` syntax
04 81 80                       ; OCTET_STRING (80 Bytes)
   38 10 60 e2 70 69 91 4a     ;   8.`.pi.J
   8b b5 22 57 2a 62 ef de     ;   .."W*b..
   15 7d 59 d6 4e 20 9a 45     ;   .}Y.N .E
   2b e3 fd fc 68 ba af bf     ;   +...h...
   9c 17 b0 8e 6d c4 29 1e     ;   ....m.).
   e3 21 ac bb 5a 8a c9 67     ;   .!..Z..g
   0a d4 45 93 10 c0 26 eb     ;   ..E...&.
   0a 83 c2 b1 40 87 36 f7     ;   ....@.6.
   a0 26 da b9 bb 46 73 88     ;   .&...Fs.
   7a 67 b9 e6 b3 6f ea 59     ;   zg...o.Y
   28 8a d3 92 72 f6 7b 89     ;   (...r.{.
   a0 d8 2d 9e 40 eb 1e bb     ;   ..-.@...
   6e ae f0 5a ed 16 c9 e3     ;   n..Z....
   27 59 37 8f f3 4a 98 60     ;   'Y7..J.`
   f8 fb a7 0a ee 1b 6e 91     ;   ......n.
   95 96 cf 0d 56 ac ab 35     ;   ....V..5
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Système de type ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codage DER des types ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



