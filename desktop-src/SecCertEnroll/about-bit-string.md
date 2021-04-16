---
description: Le type de données chaîne binaire est encodé dans un triplet TLV qui commence par un octet tag de 0x03.
ms.assetid: 7464dd20-5e79-4ca1-a6ae-9b706e9cb925
title: CHAÎNE DE BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115ead46663b94d6db2d089f1fae2fd8c40a2ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551126"
---
# <a name="bit-string"></a>CHAÎNE DE BITS

Le type de données **chaîne binaire** est encodé dans un triplet TLV qui commence par un octet **tag** de 0x03. Le champ **valeur** de l’tripleon TLV contient un octet de début qui spécifie le nombre de bits laissés inutilisés dans l’octet final du contenu. Dans l’exemple suivant, le champ de **longueur** est défini sur 0x03, car trois octets de contenu suivent, et l’octet de début du champ de **valeur** est défini sur 0x04, car il y a quatre bits inutilisés dans le dernier octet de contenu. Chaque bit inutilisé est indiqué par la lettre x.

![codage der du type de données de chaîne binaire](images/der-tlv-bitstring.png)

L’exemple suivant, adapté de la [rubrique \# ASN. 1 encodée par PKCS 10](pkcs--10-encoded-asn-1.md) , illustre la signature encodée d’un exemple de \# demande de certificat PKCS 10. Le premier octet contient la valeur de **balise** pour le type de données de **chaîne binaire** , 0x03. Le deuxième et le troisième octets contiennent la longueur du tableau d’octets. Le bit 7 du deuxième octet a la valeur 1, car il y a plus de 127 octets de contenu. Les bits 0 à 6 du deuxième octet spécifient le nombre d’octets de **longueur** de fin, dans le cas présent. Le troisième octet spécifie le nombre d’octets de contenu, 0x81. Le quatrième octet, 0x00, spécifie le nombre de bits inutilisés qui existent dans le dernier octet de contenu. Notez que la signature est encodée dans l’ordre des octets de poids fort (Big-endian).

``` syntax
0299:    03 81 81           ; BIT_STRING (81 Bytes)
029c:       00
029d:       47 eb 99 5a df 9e 70 0d  fb a7 31 32 c1 5f 5c 24
02ad:       c2 e0 bf c6 24 af 15 66  0e b8 6a 2e ab 2b c4 97
02bd:       1f e3 cb dc 63 a5 25 ec  c7 b4 28 61 66 36 a1 31
02cd:       1b bf dd d0 fc bf 17 94  90 1d e5 5e c7 11 5e c9
02dd:       55 9f eb a3 3e 14 c7 99  a6 cb ba a1 46 0f 39 d4
02ed:       44 c4 c8 4b 76 0e 20 5d  6d a9 34 9e d4 d5 87 42
02fd:       eb 24 26 51 14 90 b4 0f  06 5e 52 88 32 7a 95 20
030d:       a0 fd f7 e5 7d 60 dd 72  68 9b f5 7b 05 8f 6d 1e
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Système de type ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codage DER des types ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Octets de longueur et de valeur encodés](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 



