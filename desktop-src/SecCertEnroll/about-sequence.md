---
description: Une séquence contient un champ ordonné d’un ou plusieurs types.
ms.assetid: b1a37cde-d5a2-4b01-a076-cb09741ae51d
title: SEQUENCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1362fd66180d6f85926e1c0fe0ae57cc0edbf5edc770283ef7d9eae81cbd7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903698"
---
# <a name="sequence"></a>SEQUENCE

Une **séquence** contient un champ ordonné d’un ou plusieurs types. Elle est encodée dans un triplet TLV qui commence par un octet de **balise** de 0x30. La Certutil.exe suivante de la rubrique [ \# ASN 10 encodée ASN. 1](pkcs--10-encoded-asn-1.md) fournit plusieurs exemples de structures de données de **séquence** . La sortie affiche une clé publique de 128 octets et un exposant de trois octets.

``` syntax
30 81 9f                             ; SEQUENCE (9f Bytes)
|  30 0d                             ; SEQUENCE (d Bytes)
|  |  |  06 09                       ; OBJECT_ID (9 Bytes)
|  |  |  2a 86 48 86 f7 0d 01 01 01  ; 1.2.840.113549.1.1.1 
|  |  05 00                          ; NULL (0 Bytes)
|  03 81 8d                          ; BIT_STRING (8d Bytes)
|     00
|     30 81 89                       ; SEQUENCE (89 Bytes)
|        02 81 81                    ; INTEGER (81 Bytes)
|        |  00
|        |  8f e2 41 2a 08 e8 51 a8  8c b3 e8 53 e7 d5 49 50
|        |  b3 27 8a 2b cb ea b5 42  73 ea 02 57 cc 65 33 ee
|        |  88 20 61 a1 17 56 c1 24  18 e3 a8 08 d3 be d9 31
|        |  f3 37 0b 94 b8 cc 43 08  0b 70 24 f7 9c b1 8d 5d
|        |  d6 6d 82 d0 54 09 84 f8  9f 97 01 75 05 9c 89 d4
|        |  d5 c9 1e c9 13 d7 2a 6b  30 91 19 d6 d4 42 e0 c4
|        |  9d 7c 92 71 e1 b2 2f 5c  8d ee f0 f1 17 1e d2 5f
|        |  31 5b b1 9c bc 20 55 bf  3a 37 42 45 75 dc 90 65
|        02 03                       ; INTEGER (3 Bytes)
|           01 00 01
```

Si la **séquence** contient moins de 128 octets, le champ de **longueur** de l’tripleon TLV ne requiert qu’un octet pour spécifier la longueur du contenu. Si la valeur est supérieure à 127 octets, le bit 7 du champ de **longueur** est défini sur 1 et les bits 6 à 0 spécifient le nombre d’octets supplémentaires utilisés pour identifier la longueur du contenu. Par exemple, le deuxième octet de la première ligne de l’exemple précédent indique qu’il y a un octet de **longueur** de fin qui spécifie 0x9F octets de contenu (la majeure partie de la **séquence** n’est pas affichée). Pour plus d’informations, consultez [longueur encodée et octets de valeur](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Système de type ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codage DER des types ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



