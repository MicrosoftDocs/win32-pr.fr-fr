---
description: Le filtre d’adresse notifie au pilote Moniteur réseau d’accepter des frames ayant l’un des différents types d’adresses MAC spécifiés (Ethernet, Token Ring et FDDI).
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Écriture de la partie de filtre ADDRESSTABLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b06b00d046d555dffc39561b817629f4f47ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522194"
---
# <a name="writing-addresstable-filter-portion"></a><span data-ttu-id="4698f-103">Écriture de la partie de filtre ADDRESSTABLE</span><span class="sxs-lookup"><span data-stu-id="4698f-103">Writing ADDRESSTABLE Filter Portion</span></span>

<span data-ttu-id="4698f-104">Le filtre d’adresse notifie au pilote Moniteur réseau d’accepter des frames ayant l’un des différents types d’adresses MAC spécifiés (Ethernet, Token Ring et FDDI).</span><span class="sxs-lookup"><span data-stu-id="4698f-104">The address filter notifies the Network Monitor driver to accept frames that have one of a variety of specified MAC address types (Ethernet, Token Ring, and FDDI).</span></span> <span data-ttu-id="4698f-105">Vous pouvez spécifier un maximum de huit paires d’adresses.</span><span class="sxs-lookup"><span data-stu-id="4698f-105">You can specify a maximum of eight address pairs.</span></span> <span data-ttu-id="4698f-106">Une paire d’adresses peut spécifier une source, une destination, les deux ou aucune des deux.</span><span class="sxs-lookup"><span data-stu-id="4698f-106">An address pair can specify a source, a destination, both, or neither.</span></span>

<span data-ttu-id="4698f-107">La partie adresse du filtre est composée de deux structures : [**ADDRESSTABLE**](addresstable.md) et [**ADDRESSPAIR**](addresspair.md).</span><span class="sxs-lookup"><span data-stu-id="4698f-107">The address portion of the filter consists of two structures: [**ADDRESSTABLE**](addresstable.md) and [**ADDRESSPAIR**](addresspair.md).</span></span>

<span data-ttu-id="4698f-108">Si vous ne spécifiez aucune adresse, tous les frames transmettent le filtre d’adresse.</span><span class="sxs-lookup"><span data-stu-id="4698f-108">If you specify NO addresses, then ALL frames will pass the address filter.</span></span> <span data-ttu-id="4698f-109">Toutefois, si vous spécifiez des adresses, seuls les frames qui passent le filtre d’adresse donné seront transmis.</span><span class="sxs-lookup"><span data-stu-id="4698f-109">However, if you specify any addresses, only those frames that pass the given address filter will pass.</span></span>

<span data-ttu-id="4698f-110">La génération du filtre d’adresses implique l’allocation d’une structure [**ADDRESSTABLE**](addresstable.md) et le remplissage des membres de la structure [**ADDRESSPAIR**](addresspair.md) .</span><span class="sxs-lookup"><span data-stu-id="4698f-110">Building the address filter involves allocating an [**ADDRESSTABLE**](addresstable.md) structure and filling in members of the [**ADDRESSPAIR**](addresspair.md) structure.</span></span>

<span data-ttu-id="4698f-111">**Pour générer la partie adresse d’un filtre de capture**</span><span class="sxs-lookup"><span data-stu-id="4698f-111">**To build the address portion of a capture filter**</span></span>

1.  <span data-ttu-id="4698f-112">Utilisez l’indicateur **capturefilter \_ indicateurs \_ locaux \_ uniquement** de la structure [**capturefilter**](capturefilter.md) pour limiter la capture au trafic vers et depuis votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="4698f-112">Use the **CAPTUREFILTER\_FLAGS\_LOCAL\_ONLY** flag of the [**CAPTUREFILTER**](capturefilter.md) structure to restrict the capture to traffic to and from your local computer.</span></span>

    <span data-ttu-id="4698f-113">La définition de cet indicateur ne définit pas la carte réseau en mode promiscuité. le fichier de capture capture uniquement le trafic local.</span><span class="sxs-lookup"><span data-stu-id="4698f-113">Setting this flag will not set the NIC to promiscuous mode; the capture file will capture only local traffic.</span></span>

2.  <span data-ttu-id="4698f-114">Utilisez l’exemple de code suivant pour définir la structure [**ADDRESSTABLE**](addresstable.md) :</span><span class="sxs-lookup"><span data-stu-id="4698f-114">Use the following example code to define the [**ADDRESSTABLE**](addresstable.md) structure:</span></span>

    ``` syntax
    typedef struct _ADDRESSTABLE
    {
        DWORD           nAddressPairs;
        DWORD           nNonMacAddressPairs;
        ADDRESSPAIR     AddressPair[MAX_ADDRESS_PAIRS];
    } ADDRESSTABLE;

    typedef ADDRESSTABLE *LPADDRESSTABLE;
     
    typedef struct _ADDRESSPAIR
    {
        WORD        AddressFlags;
        WORD        NalReserved;
        ADDRESS     DstAddress;
        ADDRESS     SrcAddress;
    } ADDRESSPAIR;

    typedef ADDRESSPAIR *LPADDRESSPAIR;
    ```

3.  <span data-ttu-id="4698f-115">Utilisez les informations indiquées dans le tableau ci-dessous pour sélectionner un type d’indicateur [**ADDRESSPAIR**](addresspair.md) .</span><span class="sxs-lookup"><span data-stu-id="4698f-115">Use the information, listed in the following table, to select an [**ADDRESSPAIR**](addresspair.md) flag type.</span></span> 

    | <span data-ttu-id="4698f-116">Indicateur</span><span class="sxs-lookup"><span data-stu-id="4698f-116">Flag</span></span>                             | <span data-ttu-id="4698f-117">Signification</span><span class="sxs-lookup"><span data-stu-id="4698f-117">Meaning</span></span>                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | <span data-ttu-id="4698f-118">indicateurs d’adresse \_ \_ correspondant à l' \_ heure d’été</span><span class="sxs-lookup"><span data-stu-id="4698f-118">ADDRESS\_FLAGS\_MATCH\_DST</span></span>       | <span data-ttu-id="4698f-119">Correspond à une adresse de destination.</span><span class="sxs-lookup"><span data-stu-id="4698f-119">Matches a destination address.</span></span>                                                        |
    | <span data-ttu-id="4698f-120">indicateurs d’adresse \_ \_ correspondant à \_ src</span><span class="sxs-lookup"><span data-stu-id="4698f-120">ADDRESS\_FLAGS\_MATCH\_SRC</span></span>       | <span data-ttu-id="4698f-121">Correspond à une adresse source</span><span class="sxs-lookup"><span data-stu-id="4698f-121">Matches a source address</span></span>                                                              |
    | <span data-ttu-id="4698f-122">indicateurs d’adresse- \_ \_ exclure</span><span class="sxs-lookup"><span data-stu-id="4698f-122">ADDRESS\_FLAGS\_EXCLUDE</span></span>          | <span data-ttu-id="4698f-123">Exclut le frame si cette adresse est trouvée (une source ou une destination définie).</span><span class="sxs-lookup"><span data-stu-id="4698f-123">Excludes the frame if this address is found (either a defined source or destination).</span></span> |
    | <span data-ttu-id="4698f-124">\_identificateurs d’adresse \_ ADR du \_ groupe DST \_</span><span class="sxs-lookup"><span data-stu-id="4698f-124">ADDRESS\_FLAGS\_DST\_GROUP\_ADDR</span></span> | <span data-ttu-id="4698f-125">Correspond au bit de groupe (de l’adresse de destination) uniquement pour les messages de type diffusion.</span><span class="sxs-lookup"><span data-stu-id="4698f-125">Matches group bit (of the destination address) only for broadcast-type messages.</span></span>      |
    | <span data-ttu-id="4698f-126">\_les indicateurs d’adresse \_ correspondent à la \_ fois</span><span class="sxs-lookup"><span data-stu-id="4698f-126">ADDRESS\_FLAGS\_MATCH\_BOTH</span></span>      | <span data-ttu-id="4698f-127">Correspond à la fois à l’adresse de destination et à la source.</span><span class="sxs-lookup"><span data-stu-id="4698f-127">Matches both the destination and source addresses.</span></span>                                    |

    

     

4.  <span data-ttu-id="4698f-128">Renseignez une adresse de destination, qui est évaluée par rapport à l’indicateur [**ADDRESSPAIR**](addresspair.md) que vous sélectionnez.</span><span class="sxs-lookup"><span data-stu-id="4698f-128">Fill in a destination address, which is evaluated against the [**ADDRESSPAIR**](addresspair.md) flag that you select.</span></span>
5.  <span data-ttu-id="4698f-129">Renseignez une adresse source, qui est évaluée par rapport à l’indicateur [**ADDRESSPAIR**](addresspair.md) que vous sélectionnez.</span><span class="sxs-lookup"><span data-stu-id="4698f-129">Fill in a source address, which is evaluated against the [**ADDRESSPAIR**](addresspair.md) flag that you select.</span></span>
6.  <span data-ttu-id="4698f-130">Remplissez la structure [**ADDRESSTABLE**](addresstable.md) avec un tableau de structures [**ADDRESSPAIR**](addresspair.md) , qui comprend les paires d’adresses évaluées par le pilote.</span><span class="sxs-lookup"><span data-stu-id="4698f-130">Populate the [**ADDRESSTABLE**](addresstable.md) structure with an array of [**ADDRESSPAIR**](addresspair.md) structures, which includes the address pairs that the driver evaluates.</span></span> <span data-ttu-id="4698f-131">Toutes les paires d’adresses sont évaluées comme une instruction OR logique (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2).</span><span class="sxs-lookup"><span data-stu-id="4698f-131">All address pairs are evaluated as a logical OR statement (ADDRESSPAIR 1 \|\| ADDRESSPAIR 2).</span></span> <span data-ttu-id="4698f-132">Vous pouvez inclure un maximum de huit paires d’adresses dans un filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="4698f-132">You can include a maximum of eight address pairs in a capture filter.</span></span>

 

 



