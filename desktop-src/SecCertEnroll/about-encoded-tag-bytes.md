---
description: Le champ de balise dans un triplet de type de données identifie le type de la structure de données envoyée entre les ordinateurs.
ms.assetid: 4723cc02-8c48-488e-95b8-c646a99b6aab
title: Octets de balise encodés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5994f7beea0aba6896e94cb992a1e72eb70914
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558277"
---
# <a name="encoded-tag-bytes"></a>Octets de balise encodés

Le champ de *balise* dans un triplet de type de données identifie le type de la structure de données envoyée entre les ordinateurs. Par exemple, la balise d’un entier est 0x02, et la balise pour un identificateur d’objet est 0x06. Bien que plusieurs octets soient autorisés, aucun des types de données utilisés par l’API d’inscription de certificats n’en requiert plus d’un. L’illustration suivante montre la répartition d’une valeur de *balise* . Les bits 7 et 6 identifient la classe de balisage ASN. 1. Il existe quatre classes disponibles, mais l’API d’inscription de certificats utilise des types de données qui appartiennent uniquement à la classe universelle. Le bit 5 indique si le formulaire de codage est primitif ou construit. Les types de base et de chaîne sont encodés à l’aide de formes primitives, de types construits à l’aide d’un formulaire construit. Pour plus d’informations, consultez [système de type ASN. 1](about-asn-1-type-system.md). Les bits 4 à 0 contiennent le numéro de balise.

![octet de balise der TLV](images/der-tlv-tagbyte.png)

Le tableau suivant répertorie les types de données pris en charge par l’API d’inscription de certificats, le formulaire de codage utilisé et la valeur de balise.

| Type              | Classe ASN. 1 | Formulaire de codage | Valeur de la balise                             |
|-------------------|-------------|---------------|---------------------------------------|
| CHAÎNE DE BITS        | UNIVERSELLE   | Primitives     | 00000011<br/> 0x03<br/> |
| BOOLEAN           | UNIVERSELLE   | Primitives     | 00000001<br/> 0x01<br/> |
| INTEGER           | UNIVERSELLE   | Primitives     | 00000010<br/> 0x02<br/> |
| NULL              | UNIVERSELLE   | Primitives     | 00000101<br/> 0x05<br/> |
| IDENTIFICATEUR D’OBJET | UNIVERSELLE   | Primitives     | 00000110<br/> 0x06<br/> |
| CHAÎNE D’OCTETS      | UNIVERSELLE   | Primitives     | 00000100<br/> 0x04<br/> |
| BMPString         | UNIVERSELLE   | Primitives     | 00011110<br/> 0X1E<br/> |
| IA5String         | UNIVERSELLE   | Primitives     | 00010110<br/> (0x16)<br/> |
| PrintableString   | UNIVERSELLE   | Primitives     | 00010011<br/> 0x13<br/> |
| TeletexString     | UNIVERSELLE   | Primitives     | 00010100<br/> 0x14<br/> |
| UTF8String        | UNIVERSELLE   | Primitives     | 00001100<br/> (0x0C)<br/> |
| SEQUENCE          | UNIVERSELLE   | Constitué   | 00110000<br/> 0x30<br/> |
| SÉQUENCE DE       | UNIVERSELLE   | Constitué   | 00110000<br/> 0x30<br/> |
| SET               | UNIVERSELLE   | Constitué   | 00110001<br/> 0x31<br/> |
| ENSEMBLE DE            | UNIVERSELLE   | Constitué   | 00110001<br/> 0x31<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Syntaxe de transfert DER](about-der-transfer-syntax.md)
</dt> <dt>

[Octets de longueur et de valeur encodés](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 




