---
description: lorsque vous initialisez un objet IX500DistinguishedName avec un nom unique pour identifier le sujet d’une demande de certificat, Distinguished Encoding Rules une séquence (ASN. 1) encodée au format DER (Abstract Syntax Notation One) est créée.
ms.assetid: 58b05b59-2235-49bd-9543-45e786d62eaf
title: Encodage d’un nom de sujet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8849bda237c174fb160c862da4399fa4a734dbc74b5e6f476e1c59d22d1fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780078"
---
# <a name="encoding-a-subject-name"></a>Encodage d’un nom de sujet

lorsque vous initialisez un objet [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) avec un nom unique pour identifier le sujet d’une demande de certificat, [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) une séquence (ASN. 1) encodée au format DER ( [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) ) est créée. Par exemple, supposons que le nom unique du sujet se compose des noms distinctifs relatifs suivants :<dl> E =Administrator@jdomcsc.nttest.microsoft.com  
CN = administrateur  
CN = utilisateurs  
DC = jdomcsc  
DC = nttest  
DC = Microsoft  
DC = com  
La rubrique </dl>The **IX500DistinguishedName** object creates the following DER-encoded (ASN.1) sequence. Notice that the sequence is encoded in reverse order. This example is derived from the<a href="pkcs--7-renewal-encoded-asn-1.md">ASN. 1, encodée par le renouvellement de #7 PKCS</a> .

``` syntax
0a0d: 30 81 c4          ; SEQUENCE (c4 Bytes)
0a10: |  31 13          ; SET (13 Bytes)
0a12: |  |  30 11               ; SEQUENCE (11 Bytes)
0a14: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a16: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a20: |  |     16 03        ; IA5_STRING (3 Bytes)
0a22: |  |        63 6f 6d                                          ; com
      |  |           ; "com"
0a25: |  31 19          ; SET (19 Bytes)
0a27: |  |  30 17               ; SEQUENCE (17 Bytes)
0a29: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a2b: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a35: |  |     16 09            ; IA5_STRING (9 Bytes)
0a37: |  |        6d 69 63 72 6f 73 6f 66  74                       ; microsoft
      |  |           ; "microsoft"
0a40: |  31 16          ; SET (16 Bytes)
0a42: |  |  30 14               ; SEQUENCE (14 Bytes)
0a44: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a46: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a50: |  |     16 06            ; IA5_STRING (6 Bytes)
0a52: |  |        6e 74 74 65 73 74                                 ; nttest
      |  |           ; "nttest"
0a58: |  31 17          ; SET (17 Bytes)
0a5a: |  |  30 15               ; SEQUENCE (15 Bytes)
0a5c: |  |     06 0a            ; OBJECT_ID (a Bytes)
0a5e: |  |     |  09 92 26 89 93 f2 2c 64  01 19
      |  |     |     ; 0.9.2342.19200300.100.1.25 Domain Component (DC)
0a68: |  |     16 07            ; IA5_STRING (7 Bytes)
0a6a: |  |        6a 64 6f 6d 63 73 63                              ; jdomcsc
      |  |           ; "jdomcsc"
0a71: |  31 0e          ; SET (e Bytes)
0a73: |  |  30 0c               ; SEQUENCE (c Bytes)
0a75: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a77: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a7a: |  |     13 05            ; PRINTABLE_STRING (5 Bytes)
0a7c: |  |        55 73 65 72 73                                    ; Users
      |  |           ; "Users"
0a81: |  31 16          ; SET (16 Bytes)
0a83: |  |  30 14               ; SEQUENCE (14 Bytes)
0a85: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a87: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a8a: |  |     13 0d            ; PRINTABLE_STRING (d Bytes)
0a8c: |  |        41 64 6d 69 6e 69 73 74  72 61 74 6f 72           ; Administrator
      |  |           ; "Administrator"
0a99: |  31 39          ; SET (39 Bytes)
0a9b: |     30 37               ; SEQUENCE (37 Bytes)
0a9d: |        06 09            ; OBJECT_ID (9 Bytes)
0a9f: |        |  2a 86 48 86 f7 0d 01 09  01
      |        |     ; 1.2.840.113549.1.9.1 Email Address (E)
0aa8: |        16 2a            ; IA5_STRING (2a Bytes)
0aaa: |           41 64 6d 69 6e 69 73 74  72 61 74 6f 72 40 6a 64  ; Administrator@jd
0aba: |           6f 6d 63 73 63 2e 6e 74  74 65 73 74 2e 6d 69 63  ; omcsc.nttest.mic
0aca: |           72 6f 73 6f 66 74 2e 63  6f 6d                    ; rosoft.com
      |              ; "Administrator@jdomcsc.nttest.microsoft.com"
```

Comme indiqué dans [noms d’objet](subject-names.md), chaque RDN dans un nom unique se compose d’un ensemble d’attributs, et chaque attribut contient un [*identificateur d’objet*](/windows/desktop/SecGloss/o-gly) (OID) et une valeur. Pour comprendre comment l’objet [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) encode un nom unique, considérez le nom commun CN = Users.

``` syntax
0a73: |  |  30 0c               ; SEQUENCE (c Bytes)
0a75: |  |     06 03            ; OBJECT_ID (3 Bytes)
0a77: |  |     |  55 04 03
      |  |     |     ; 2.5.4.3 Common Name (CN)
0a7a: |  |     13 05            ; PRINTABLE_STRING (5 Bytes)
0a7c: |  |        55 73 65 72 73                                    ; Users
      |  |           ; "Users"
```

La syntaxe de transfert DER d’un objet ASN. 1 contient toujours un type, une longueur et un triplet de valeur, et chaque champ de l’triplet contient un ou plusieurs octets. En cas d’encodage, CN = Users se compose d’un OID et d’une valeur de chaîne. La notation décimale séparée par des points de l’OID CN est 2.5.4.3 et la valeur de chaîne est « Users ». La valeur de chaîne est représentée sous la forme d’un type de données **PRINTABLE_STRING** . La valeur de type numérique associée à **object_id** est toujours 0x06, et le type numérique associé à **PRINTABLE_STRING** est toujours 0x13. La longueur du nom commun « Users » est 0x05 octets. La longueur de l’OID est de 0x03 octets et sa valeur est 0x55 0x04 0x03.

> [!Note]  
> Pour convertir les deux premiers chiffres du 2.5.4.3 OID en valeur hexadécimale 0x55, multipliez le premier chiffre de l’OID par 40 (2 x 40) et ajoutez le deuxième chiffre (5) avant de convertir au format hexadécimal.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fichier \# ASN. 1 de renouvellement PKCS 7](pkcs--7-renewal-encoded-asn-1.md)
</dt> <dt>

[Exemples de demandes](sample-requests.md)
</dt> <dt>

[Noms de sujets](subject-names.md)
</dt> </dl>

 

 
