---
description: Le type de données de l’identificateur d’objet est encodé dans un triplet TLV qui commence par une valeur de balise 0x06.
ms.assetid: 42c015c8-3de1-4482-bf27-b19c422b8cdb
title: IDENTIFICATEUR D’OBJET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cc81169968bfb3be5a49b0f30b8171cd904bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202842"
---
# <a name="object-identifier"></a>IDENTIFICATEUR D’OBJET

Le type de données de l' **identificateur d’objet** est encodé dans un triplet TLV qui commence par une valeur de **balise** 0x06. Chaque entier d’un identificateur d’objet décimal pointé (OID) est encodé selon les règles suivantes :

-   Les deux premiers nœuds de l’OID sont encodés sur un seul octet. Le premier nœud est multiplié par la valeur décimale 40 et le résultat est ajouté à la valeur du deuxième nœud.
-   Les valeurs de nœud inférieures ou égales à 127 sont encodées sur un octet.
-   Les valeurs de nœud supérieures ou égales à 128 sont encodées sur plusieurs octets. Le bit 7 de l’octet le plus à gauche est défini sur un. Les bits 0 à 6 de chaque octet contiennent la valeur encodée.

Ces points sont indiqués dans l’illustration suivante.

![codage der du type de données de l’identificateur d’objet](images/der-tlv-oid.png)

L’exemple suivant montre comment l’attribut **ClientID** est encodé dans une demande de certificat.

``` syntax
06 09                                ; OBJECT_ID (9 Bytes)
|  2b 06 01 04 01 82 37 15  14       ;   1.3.6.1.4.1.311.21.20 
31 4a                                ; SET (4a Bytes)
   30 48                             ; SEQUENCE (48 Bytes)
      02 01                          ; INTEGER (1 Bytes)
      |  09
      0c 23                          ; UTF8_STRING (23 Bytes)
      |  76 69 63 68 33 64 2e 6a     ;   vich3d.j
      |  64 6f 6d 63 73 63 2e 6e     ;   domcsc.n
      |  74 74 65 73 74 2e 6d 69     ;   ttest.mi
      |  63 72 6f 73 6f 66 74 2e     ;   crosoft.
      |  63 6f 6d                    ;   com
      0c 15                          ; UTF8_STRING (15 Bytes)
      |  4a 44 4f 4d 43 53 43 5c     ;   JDOMCSC\
      |  61 64 6d 69 6e 69 73 74     ;   administ
      |  72 61 74 6f 72              ;   rator
      0c 07                          ; UTF8_STRING (7 Bytes)
         63 65 72 74 72 65 71        ;   certreq
```

 

 



