---
description: Le type de données ASN. 1 UTF8String est encodé dans un triplet TLV qui commence par un octet tag de 0x0C.
ms.assetid: e30737d3-8294-48d8-9e42-f21918acc73c
title: UTF8String
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26048a46689d27b68e8cacfa4af13b37cde4d613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865021"
---
# <a name="utf8string"></a><span data-ttu-id="cfe5d-103">UTF8String</span><span class="sxs-lookup"><span data-stu-id="cfe5d-103">UTF8String</span></span>

<span data-ttu-id="cfe5d-104">Le type de données ASN. 1 **UTF8String** est encodé dans un triplet TLV qui commence par un octet **tag** de 0x0C.</span><span class="sxs-lookup"><span data-stu-id="cfe5d-104">The ASN.1 **UTF8String** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x0C.</span></span> <span data-ttu-id="cfe5d-105">L’exemple suivant, issu de la rubrique [ASN. 1 encodée par CMC](cmc-encoded-asn-1.md) , montre comment l’attribut **ClientID** est encodé sous la forme d’un entier et de trois types **UTF8String** .</span><span class="sxs-lookup"><span data-stu-id="cfe5d-105">The following example, from the [CMC Encoded ASN.1](cmc-encoded-asn-1.md) topic, shows how the **ClientId** attribute is encoded as an integer and three **UTF8String** types.</span></span> <span data-ttu-id="cfe5d-106">L’identificateur d’objet pour l’attribut est 1.3.6.1.4.1.311.21.20.</span><span class="sxs-lookup"><span data-stu-id="cfe5d-106">The object identifier for the attribute is 1.3.6.1.4.1.311.21.20.</span></span> <span data-ttu-id="cfe5d-107">Les informations, qui peuvent être spécifiées à l’aide de l’interface [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) , incluent un numéro d’ID client, le nom d’ordinateur DNS (Domain Name System), le nom d’utilisateur Sam (Security Accounts Manager) et le nom de l’application qui a créé la demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="cfe5d-107">The information, which can be specified by using the [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) interface, includes a client ID number, the Domain Name System (DNS) computer name, the Security Accounts Manager (SAM) user name, and the name of the application that created the certificate request.</span></span>

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

<span data-ttu-id="cfe5d-108">Si la chaîne contient moins de 128 octets, le champ de **longueur** de l’tripleon TLV ne requiert qu’un octet pour spécifier la longueur du contenu.</span><span class="sxs-lookup"><span data-stu-id="cfe5d-108">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="cfe5d-109">Si la chaîne est supérieure à 127 octets, le bit 7 du champ de **longueur** est défini sur 1 et les bits 6 à 0 spécifient le nombre d’octets supplémentaires utilisés pour identifier la longueur du contenu.</span><span class="sxs-lookup"><span data-stu-id="cfe5d-109">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="cfe5d-110">Pour plus d’informations, consultez [longueur encodée et octets de valeur](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="cfe5d-110">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cfe5d-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cfe5d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfe5d-112">Système de type ASN. 1</span><span class="sxs-lookup"><span data-stu-id="cfe5d-112">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="cfe5d-113">Codage DER des types ASN. 1</span><span class="sxs-lookup"><span data-stu-id="cfe5d-113">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



