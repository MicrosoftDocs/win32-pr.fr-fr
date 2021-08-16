---
description: Les valeurs entières sont encodées dans un triplet TLV qui commence par une valeur de balise 0x02.
ms.assetid: a6fed62f-af59-488c-a690-be8c3413086f
title: ENTIER (API d’inscription de certificats)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85151947653a66c98b7a030ade7b9ff7b4f5ee87fd84edc4cc52679be296a1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904340"
---
# <a name="integer-certificate-enrollment-api"></a>ENTIER (API d’inscription de certificats)

Les valeurs entières sont encodées dans un triplet TLV qui commence par une valeur de **balise** 0x02. Le champ de **valeur** de l’tripleon TLV contient l’entier encodé s’il est positif, ou son complément à deux s’il est négatif. Si l’entier est positif mais que le bit de poids fort a la valeur 1, un 0x00 de début est ajouté au contenu pour indiquer que le nombre n’est pas négatif. Par exemple, l’octet de poids fort de 0x8F (10001111) est 1. Par conséquent, un octet zéro non significatif est ajouté au contenu comme indiqué dans l’illustration suivante.

![codage der de type de données booléen](images/der-tlv-integer.png)

Si l’entier contient moins de 128 octets, le champ de *longueur* ne requiert qu’un octet pour spécifier la longueur du contenu. Si l’entier est supérieur à 127 octets, le bit 7 du champ de *longueur* est défini sur 1 et les bits 6 à 0 spécifient le nombre d’octets supplémentaires utilisés pour identifier la longueur du contenu. Pour plus d’informations, consultez [longueur encodée et octets de valeur](about-encoded-length-and-value-bytes.md).

L’exemple suivant, issu du fichier [ \# ASN. 1 encodé par PKCS 10](pkcs--10-encoded-asn-1.md), illustre l’encodage d’une clé publique de 128 octets. Le premier octet contient la valeur de **balise** pour le type de données **Integer** , 0x02. Le deuxième et le troisième octets contiennent la valeur de **longueur** . Le bit 7 du deuxième octet a la valeur 1, car il y a plus de 127 octets de contenu. Les bits 0 à 6 du deuxième octet spécifient le nombre d’octets de fin nécessaires, dans ce cas un, pour spécifier avec précision la longueur du contenu. Le troisième octet spécifie le nombre d’octets de contenu, 0x81. Le quatrième octet, 0x00, est ajouté au contenu pour indiquer que l’entier est effectivement une valeur positive, même si le bit de signe de l’octet de début (0x8F) est défini sur 1.

``` syntax
02 81 81          ; INTEGER (81 Bytes)
|  00
|  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
```

L’exemple suivant montre comment la valeur entière 0x03 est encodée. L’octet de la **balise** contient 0x02 et l’octet de **longueur** spécifie qu’il y a un octet de contenu.

``` syntax
02 01             ; INTEGER (1 Bytes)
|  03
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Système de type ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codage DER des types ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



