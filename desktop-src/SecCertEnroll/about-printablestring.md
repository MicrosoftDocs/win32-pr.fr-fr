---
description: Le type de données ASN. 1 PrintableString est encodé dans un triplet TLV qui commence par un octet de balise 0x13.
ms.assetid: 998fef66-7a24-462f-96f2-92c739bbefa2
title: PrintableString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ebc95f1a58e8d7beb4a1d3bbb037788252349a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865025"
---
# <a name="printablestring"></a><span data-ttu-id="53784-103">PrintableString</span><span class="sxs-lookup"><span data-stu-id="53784-103">PrintableString</span></span>

<span data-ttu-id="53784-104">Le type de données ASN. 1 **printableString** est encodé dans un triplet TLV qui commence par un octet de **balise** 0x13.</span><span class="sxs-lookup"><span data-stu-id="53784-104">The ASN.1 **PrintableString** data type is encoded into a TLV triplet that begins with a **Tag** byte of 0x13.</span></span> <span data-ttu-id="53784-105">L’exemple suivant, issu de la rubrique [ \# ASN. 1 encodée par PKCS 10](pkcs--10-encoded-asn-1.md) , montre comment un nom commun d’utilisateur TestCN est encodé en tant que type **printableString** .</span><span class="sxs-lookup"><span data-stu-id="53784-105">The following example, from the [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md) topic, shows how a user common name of TestCN is encoded as a **PrintableString** type.</span></span> <span data-ttu-id="53784-106">L’identificateur d’objet pour un nom commun est 2.5.4.3.</span><span class="sxs-lookup"><span data-stu-id="53784-106">The object identifier for a common name is 2.5.4.3.</span></span>

``` syntax
06 03                   ; OBJECT_ID (3 Bytes)
|  55 04 03             ;   2.5.4.3 Common Name (CN)
13 06                   ; PRINTABLE_STRING (6 Bytes)
   54 65 73 74 43 4e    ;   TestCN
```

<span data-ttu-id="53784-107">Si la chaîne contient moins de 128 octets, le champ de **longueur** de l’tripleon TLV ne requiert qu’un octet pour spécifier la longueur du contenu.</span><span class="sxs-lookup"><span data-stu-id="53784-107">If the string contains fewer than 128 bytes, the **Length** field of the TLV triplet requires only one byte to specify the content length.</span></span> <span data-ttu-id="53784-108">Si la chaîne est supérieure à 127 octets, le bit 7 du champ de **longueur** est défini sur 1 et les bits 6 à 0 spécifient le nombre d’octets supplémentaires utilisés pour identifier la longueur du contenu.</span><span class="sxs-lookup"><span data-stu-id="53784-108">If the string is more than 127 bytes, bit 7 of the **Length** field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="53784-109">Pour plus d’informations, consultez [longueur encodée et octets de valeur](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="53784-109">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="53784-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="53784-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53784-111">Système de type ASN. 1</span><span class="sxs-lookup"><span data-stu-id="53784-111">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="53784-112">Codage DER des types ASN. 1</span><span class="sxs-lookup"><span data-stu-id="53784-112">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



