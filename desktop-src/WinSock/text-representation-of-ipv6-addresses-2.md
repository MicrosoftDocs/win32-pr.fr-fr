---
description: Cette section est copiée à partir de &\# 0034 ; architecture d’adressage IPv6&\# 0034 ; par R.
ms.assetid: 52faecb9-0d7a-40fa-a021-3cc6816a4db8
title: Représentation textuelle des adresses IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df97c1c8933f3708fee56e34e05f918d531d2a13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536139"
---
# <a name="text-representation-of-ipv6-addresses"></a><span data-ttu-id="7f623-103">Représentation textuelle des adresses IPv6</span><span class="sxs-lookup"><span data-stu-id="7f623-103">Text Representation of IPv6 Addresses</span></span>

<span data-ttu-id="7f623-104">Cette section est copiée à partir de « architecture d’adressage IPv6 » par R. Hinden et S. Deering.</span><span class="sxs-lookup"><span data-stu-id="7f623-104">This section is copied from "IPv6 Addressing Architecture" by R. Hinden and S. Deering.</span></span> <span data-ttu-id="7f623-105">Il existe trois formes conventionnelles pour représenter les adresses IPv6 en tant que chaînes de texte :</span><span class="sxs-lookup"><span data-stu-id="7f623-105">There are three conventional forms for representing IPv6 addresses as text strings:</span></span>

-   <span data-ttu-id="7f623-106">La forme préférée est x :x: x :x: x :x: x :x, où les « x » sont les valeurs hexadécimales des parties 8 16 bits de l’adresse.</span><span class="sxs-lookup"><span data-stu-id="7f623-106">The preferred form is x:x:x:x:x:x:x:x, where the 'x's are the hexadecimal values of the eight 16-bit pieces of the address.</span></span>

    <span data-ttu-id="7f623-107">Exemples :</span><span class="sxs-lookup"><span data-stu-id="7f623-107">Examples:</span></span>

    <dl> <span data-ttu-id="7f623-108">FEDC : BA98:7654:3210 : FEDC : BA98:7654:3210</span><span class="sxs-lookup"><span data-stu-id="7f623-108">FEDC:BA98:7654:3210:FEDC:BA98:7654:3210</span></span>  
    <span data-ttu-id="7f623-109">1080:0 : 0:0 : 8:800:200C : 417A</span><span class="sxs-lookup"><span data-stu-id="7f623-109">1080:0:0:0:8:800:200C:417A</span></span>  
    </dl>

> [!Note]  
> <span data-ttu-id="7f623-110">Il n’est pas nécessaire d’écrire les zéros non significatifs dans un champ individuel, mais il doit y avoir au moins un chiffre dans chaque champ (sauf dans le cas décrit dans le deuxième formulaire).</span><span class="sxs-lookup"><span data-stu-id="7f623-110">It is not necessary to write the leading zeros in an individual field, but there must be at least one numeral in every field (except for the case described in the second form).</span></span>

 

-   <span data-ttu-id="7f623-111">En raison de la méthode d’allocation de certains styles d’adresses IPv6, il est courant que les adresses contiennent des chaînes longues de zéro bits.</span><span class="sxs-lookup"><span data-stu-id="7f623-111">Due to the method of allocating certain styles of IPv6 addresses, it is common for addresses to contain long strings of zero bits.</span></span> <span data-ttu-id="7f623-112">Pour faciliter l’écriture d’adresses contenant zéro bits, une syntaxe spéciale est disponible pour compresser les zéros.</span><span class="sxs-lookup"><span data-stu-id="7f623-112">In order to make writing addresses containing zero bits easier, a special syntax is available to compress the zeros.</span></span> <span data-ttu-id="7f623-113">L’utilisation de deux-points («  :: ») indique plusieurs groupes de zéros de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="7f623-113">The use of double colons ("::") indicates multiple groups of 16-bits of zeros.</span></span>

    <span data-ttu-id="7f623-114">Par exemple, l’adresse de multidiffusion</span><span class="sxs-lookup"><span data-stu-id="7f623-114">For example, the multicast address</span></span>

    <dl> <span data-ttu-id="7f623-115">FF01:0 : 0:0 : 0:0 : 0:0 : 43</span><span class="sxs-lookup"><span data-stu-id="7f623-115">FF01:0:0:0:0:0:0:43</span></span>  
    </dl>

    <span data-ttu-id="7f623-116">peut être représenté comme suit :</span><span class="sxs-lookup"><span data-stu-id="7f623-116">may be represented as:</span></span>

    <dl> <span data-ttu-id="7f623-117">FF01 :: 43</span><span class="sxs-lookup"><span data-stu-id="7f623-117">FF01::43</span></span>  
    </dl>

    <span data-ttu-id="7f623-118">Les guillemets doubles (" ::") ne peuvent apparaître qu’une seule fois dans une adresse.</span><span class="sxs-lookup"><span data-stu-id="7f623-118">The double quotation marks ("::") can only appear once in an address.</span></span> <span data-ttu-id="7f623-119">Elles peuvent être utilisées pour compresser des zéros de début ou de fin dans une adresse.</span><span class="sxs-lookup"><span data-stu-id="7f623-119">They can be used to compress leading or trailing zeros in an address.</span></span>

-   <span data-ttu-id="7f623-120">Une autre forme qui peut être plus pratique pour gérer un environnement mixte de nœuds IPv4 et IPv6 est x :x: x :x: x :x: d. d. d. d, où les valeurs « x » sont les valeurs hexadécimales des six parties de l’adresse (16 bits) de poids fort, et les valeurs décimales des quatre éléments 8 bits de poids faible de l’adresse (représentation IPv4 standard).</span><span class="sxs-lookup"><span data-stu-id="7f623-120">An alternative form that may be more convenient when dealing with a mixed environment of IPv4 and IPv6 nodes is x:x:x:x:x:x:d.d.d.d, where the 'x's are the hexadecimal values of the six high-order 16-bit pieces of the address, and the 'd's are the decimal values of the four low-order 8-bit pieces of the address (standard IPv4 representation).</span></span>

    <span data-ttu-id="7f623-121">Exemples :</span><span class="sxs-lookup"><span data-stu-id="7f623-121">Examples:</span></span>

    <dl> <span data-ttu-id="7f623-122">0:0 : 0:0 : 0:0 : 0:13.1.68.3</span><span class="sxs-lookup"><span data-stu-id="7f623-122">0:0:0:0:0:0:13.1.68.3</span></span>  
    <span data-ttu-id="7f623-123">0:0 : 0:0 : 0 : FFFF : 129.144.52.38</span><span class="sxs-lookup"><span data-stu-id="7f623-123">0:0:0:0:0:FFFF:129.144.52.38</span></span>  
    </dl>

    <span data-ttu-id="7f623-124">ou sous forme compressée :</span><span class="sxs-lookup"><span data-stu-id="7f623-124">or in compressed form:</span></span>

    <dl> <span data-ttu-id="7f623-125">::13.1.68.3</span><span class="sxs-lookup"><span data-stu-id="7f623-125">::13.1.68.3</span></span>  
    <span data-ttu-id="7f623-126">:: FFFF : 129.144.52.38</span><span class="sxs-lookup"><span data-stu-id="7f623-126">::FFFF:129.144.52.38</span></span>  
    </dl>

 

 



