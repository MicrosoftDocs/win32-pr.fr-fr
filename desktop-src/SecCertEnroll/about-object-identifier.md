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
# <a name="object-identifier"></a><span data-ttu-id="9cb34-103">IDENTIFICATEUR D’OBJET</span><span class="sxs-lookup"><span data-stu-id="9cb34-103">OBJECT IDENTIFIER</span></span>

<span data-ttu-id="9cb34-104">Le type de données de l' **identificateur d’objet** est encodé dans un triplet TLV qui commence par une valeur de **balise** 0x06.</span><span class="sxs-lookup"><span data-stu-id="9cb34-104">The **OBJECT IDENTIFIER** data type is encoded into a TLV triplet that begins with a **Tag** value of 0x06.</span></span> <span data-ttu-id="9cb34-105">Chaque entier d’un identificateur d’objet décimal pointé (OID) est encodé selon les règles suivantes :</span><span class="sxs-lookup"><span data-stu-id="9cb34-105">Each integer of a dotted decimal object identifier (OID) is encoded according to the following rules:</span></span>

-   <span data-ttu-id="9cb34-106">Les deux premiers nœuds de l’OID sont encodés sur un seul octet.</span><span class="sxs-lookup"><span data-stu-id="9cb34-106">The first two nodes of the OID are encoded onto a single byte.</span></span> <span data-ttu-id="9cb34-107">Le premier nœud est multiplié par la valeur décimale 40 et le résultat est ajouté à la valeur du deuxième nœud.</span><span class="sxs-lookup"><span data-stu-id="9cb34-107">The first node is multiplied by the decimal 40 and the result is added to the value of the second node.</span></span>
-   <span data-ttu-id="9cb34-108">Les valeurs de nœud inférieures ou égales à 127 sont encodées sur un octet.</span><span class="sxs-lookup"><span data-stu-id="9cb34-108">Node values less than or equal to 127 are encoded on one byte.</span></span>
-   <span data-ttu-id="9cb34-109">Les valeurs de nœud supérieures ou égales à 128 sont encodées sur plusieurs octets.</span><span class="sxs-lookup"><span data-stu-id="9cb34-109">Node values greater than or equal to 128 are encoded on multiple bytes.</span></span> <span data-ttu-id="9cb34-110">Le bit 7 de l’octet le plus à gauche est défini sur un.</span><span class="sxs-lookup"><span data-stu-id="9cb34-110">Bit 7 of the leftmost byte is set to one.</span></span> <span data-ttu-id="9cb34-111">Les bits 0 à 6 de chaque octet contiennent la valeur encodée.</span><span class="sxs-lookup"><span data-stu-id="9cb34-111">Bits 0 through 6 of each byte contains the encoded value.</span></span>

<span data-ttu-id="9cb34-112">Ces points sont indiqués dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="9cb34-112">These points are shown by the following illustration.</span></span>

![codage der du type de données de l’identificateur d’objet](images/der-tlv-oid.png)

<span data-ttu-id="9cb34-114">L’exemple suivant montre comment l’attribut **ClientID** est encodé dans une demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="9cb34-114">The following example shows how the **ClientId** attribute is encoded in a certificate request.</span></span>

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

 

 



