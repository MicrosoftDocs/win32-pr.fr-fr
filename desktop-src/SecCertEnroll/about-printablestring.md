---
description: Le type de données ASN. 1 PrintableString est encodé dans un triplet TLV qui commence par un octet de balise 0x13.
ms.assetid: 998fef66-7a24-462f-96f2-92c739bbefa2
title: PrintableString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e2714013c037e834a7c083c7ab89fcdafd59e1306226af25fcb4b6edc8b0af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903751"
---
# <a name="printablestring"></a>PrintableString

Le type de données ASN. 1 **printableString** est encodé dans un triplet TLV qui commence par un octet de **balise** 0x13. L’exemple suivant, issu de la rubrique [ \# ASN. 1 encodée par PKCS 10](pkcs--10-encoded-asn-1.md) , montre comment un nom commun d’utilisateur TestCN est encodé en tant que type **printableString** . L’identificateur d’objet pour un nom commun est 2.5.4.3.

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

Si la chaîne contient moins de 128 octets, le champ de **longueur** de l’tripleon TLV ne requiert qu’un octet pour spécifier la longueur du contenu. Si la chaîne est supérieure à 127 octets, le bit 7 du champ de **longueur** est défini sur 1 et les bits 6 à 0 spécifient le nombre d’octets supplémentaires utilisés pour identifier la longueur du contenu. Pour plus d’informations, consultez [longueur encodée et octets de valeur](about-encoded-length-and-value-bytes.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Système de type ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codage DER des types ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



