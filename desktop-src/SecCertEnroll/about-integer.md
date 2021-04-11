---
description: Les valeurs entières sont encodées dans un triplet TLV qui commence par une valeur de balise 0x02.
ms.assetid: a6fed62f-af59-488c-a690-be8c3413086f
title: ENTIER (API d’inscription de certificats)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0e8ed162d4cf4b2ac4909baf1cd7b5e94ddea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319150"
---
# <a name="integer-certificate-enrollment-api"></a><span data-ttu-id="693df-103">ENTIER (API d’inscription de certificats)</span><span class="sxs-lookup"><span data-stu-id="693df-103">INTEGER (Certificate Enrollment API)</span></span>

<span data-ttu-id="693df-104">Les valeurs entières sont encodées dans un triplet TLV qui commence par une valeur de **balise** 0x02.</span><span class="sxs-lookup"><span data-stu-id="693df-104">Integer values are encoded into a TLV triplet that begins with a **Tag** value of 0x02.</span></span> <span data-ttu-id="693df-105">Le champ de **valeur** de l’tripleon TLV contient l’entier encodé s’il est positif, ou son complément à deux s’il est négatif.</span><span class="sxs-lookup"><span data-stu-id="693df-105">The **Value** field of the TLV triplet contains the encoded integer if it is positive, or its two's complement if it is negative.</span></span> <span data-ttu-id="693df-106">Si l’entier est positif mais que le bit de poids fort a la valeur 1, un 0x00 de début est ajouté au contenu pour indiquer que le nombre n’est pas négatif.</span><span class="sxs-lookup"><span data-stu-id="693df-106">If the integer is positive but the high order bit is set to 1, a leading 0x00 is added to the content to indicate that the number is not negative.</span></span> <span data-ttu-id="693df-107">Par exemple, l’octet de poids fort de 0x8F (10001111) est 1.</span><span class="sxs-lookup"><span data-stu-id="693df-107">For example, the high order byte of 0x8F (10001111) is 1.</span></span> <span data-ttu-id="693df-108">Par conséquent, un octet zéro non significatif est ajouté au contenu comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="693df-108">Therefore a leading zero byte is added to the content as shown in the following illustration.</span></span>

![codage der de type de données booléen](images/der-tlv-integer.png)

<span data-ttu-id="693df-110">Si l’entier contient moins de 128 octets, le champ de *longueur* ne requiert qu’un octet pour spécifier la longueur du contenu.</span><span class="sxs-lookup"><span data-stu-id="693df-110">If the integer contains fewer than 128 bytes, the *Length* field requires only one byte to specify the content length.</span></span> <span data-ttu-id="693df-111">Si l’entier est supérieur à 127 octets, le bit 7 du champ de *longueur* est défini sur 1 et les bits 6 à 0 spécifient le nombre d’octets supplémentaires utilisés pour identifier la longueur du contenu.</span><span class="sxs-lookup"><span data-stu-id="693df-111">If the integer is more than 127 bytes, bit 7 of the *Length* field is set to 1 and bits 6 through 0 specify the number of additional bytes used to identify the content length.</span></span> <span data-ttu-id="693df-112">Pour plus d’informations, consultez [longueur encodée et octets de valeur](about-encoded-length-and-value-bytes.md).</span><span class="sxs-lookup"><span data-stu-id="693df-112">For more information, see [Encoded Length and Value Bytes](about-encoded-length-and-value-bytes.md).</span></span>

<span data-ttu-id="693df-113">L’exemple suivant, issu du fichier [ \# ASN. 1 encodé par PKCS 10](pkcs--10-encoded-asn-1.md), illustre l’encodage d’une clé publique de 128 octets.</span><span class="sxs-lookup"><span data-stu-id="693df-113">The following example, from [PKCS \#10 Encoded ASN.1](pkcs--10-encoded-asn-1.md), shows the encoding for a 128 byte public key.</span></span> <span data-ttu-id="693df-114">Le premier octet contient la valeur de **balise** pour le type de données **Integer** , 0x02.</span><span class="sxs-lookup"><span data-stu-id="693df-114">The first byte contains the **Tag** value for the **INTEGER** data type, 0x02.</span></span> <span data-ttu-id="693df-115">Le deuxième et le troisième octets contiennent la valeur de **longueur** .</span><span class="sxs-lookup"><span data-stu-id="693df-115">The second and third bytes contain the **Length** value.</span></span> <span data-ttu-id="693df-116">Le bit 7 du deuxième octet a la valeur 1, car il y a plus de 127 octets de contenu.</span><span class="sxs-lookup"><span data-stu-id="693df-116">Bit 7 of the second byte is set to 1 because there are more than 127 bytes of content.</span></span> <span data-ttu-id="693df-117">Les bits 0 à 6 du deuxième octet spécifient le nombre d’octets de fin nécessaires, dans ce cas un, pour spécifier avec précision la longueur du contenu.</span><span class="sxs-lookup"><span data-stu-id="693df-117">Bits 0 through 6 of the second byte specify the number of trailing bytes needed, in this case one, to accurately specify the content length.</span></span> <span data-ttu-id="693df-118">Le troisième octet spécifie le nombre d’octets de contenu, 0x81.</span><span class="sxs-lookup"><span data-stu-id="693df-118">The third byte specifies the number of content bytes, 0x81.</span></span> <span data-ttu-id="693df-119">Le quatrième octet, 0x00, est ajouté au contenu pour indiquer que l’entier est effectivement une valeur positive, même si le bit de signe de l’octet de début (0x8F) est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="693df-119">The fourth byte, 0x00, is added to the content to indicate that the integer is indeed a positive value even though the sign bit of the leading content byte (0x8F) is set to 1.</span></span>

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

<span data-ttu-id="693df-120">L’exemple suivant montre comment la valeur entière 0x03 est encodée.</span><span class="sxs-lookup"><span data-stu-id="693df-120">The following example shows how the integer value 0x03 is encoded.</span></span> <span data-ttu-id="693df-121">L’octet de la **balise** contient 0x02 et l’octet de **longueur** spécifie qu’il y a un octet de contenu.</span><span class="sxs-lookup"><span data-stu-id="693df-121">The **Tag** byte contains 0x02, and the **Length** byte specifies that there is one byte of content.</span></span>

``` syntax
02 01             ; INTEGER (1 Bytes)
|  03
```

## <a name="related-topics"></a><span data-ttu-id="693df-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="693df-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="693df-123">Système de type ASN. 1</span><span class="sxs-lookup"><span data-stu-id="693df-123">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="693df-124">Codage DER des types ASN. 1</span><span class="sxs-lookup"><span data-stu-id="693df-124">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



