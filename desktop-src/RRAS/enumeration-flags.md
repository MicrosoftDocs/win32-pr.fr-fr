---
title: Indicateurs d’énumération
description: Indicateurs d’énumération
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Énumération
- Indicateurs d’énumération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1cbec08496ccd6338de77ebdddf76547a48258
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939973"
---
# <a name="enumeration-flags"></a><span data-ttu-id="51aa7-105">Indicateurs d’énumération</span><span class="sxs-lookup"><span data-stu-id="51aa7-105">Enumeration Flags</span></span>



| <span data-ttu-id="51aa7-106">Constante</span><span class="sxs-lookup"><span data-stu-id="51aa7-106">Constant</span></span>               | <span data-ttu-id="51aa7-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="51aa7-107">Value</span></span>      | <span data-ttu-id="51aa7-108">Description</span><span class="sxs-lookup"><span data-stu-id="51aa7-108">Description</span></span>                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51aa7-109">début de l' \_ énumération RTM \_</span><span class="sxs-lookup"><span data-stu-id="51aa7-109">RTM\_ENUM\_START</span></span>       | <span data-ttu-id="51aa7-110">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51aa7-110">0x00000000</span></span> | <span data-ttu-id="51aa7-111">Énumérer les itinéraires ou les destinations à partir de 0/0.</span><span class="sxs-lookup"><span data-stu-id="51aa7-111">Enumerate routes or destinations starting at 0/0.</span></span>                                                                                                         |
| <span data-ttu-id="51aa7-112">\_énumération RTM \_ suivante</span><span class="sxs-lookup"><span data-stu-id="51aa7-112">RTM\_ENUM\_NEXT</span></span>        | <span data-ttu-id="51aa7-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="51aa7-113">0x00000001</span></span> | <span data-ttu-id="51aa7-114">Énumérer les itinéraires ou les destinations à partir de la longueur d’adresse/de masque spécifiée (par exemple, 10/8).</span><span class="sxs-lookup"><span data-stu-id="51aa7-114">Enumerate routes or destinations starting at the specified address/mask length (such as 10/8).</span></span> <span data-ttu-id="51aa7-115">L’énumération continue jusqu’à la fin de la table de routage.</span><span class="sxs-lookup"><span data-stu-id="51aa7-115">The enumeration continues to the end of the routing table.</span></span> |
| <span data-ttu-id="51aa7-116">\_plage d’énumération RTM \_</span><span class="sxs-lookup"><span data-stu-id="51aa7-116">RTM\_ENUM\_RANGE</span></span>       | <span data-ttu-id="51aa7-117">0x00000002</span><span class="sxs-lookup"><span data-stu-id="51aa7-117">0x00000002</span></span> | <span data-ttu-id="51aa7-118">Énumérer les itinéraires ou les destinations dans la sous-arborescence spécifiée spécifiée par la longueur de l’adresse/du masque (par exemple, 10/8).</span><span class="sxs-lookup"><span data-stu-id="51aa7-118">Enumerate routes or destinations in the specified subtree specified by the address/mask length (such as 10/8).</span></span>                                            |
| <span data-ttu-id="51aa7-119">\_enum RTM \_ toutes les \_ dest.</span><span class="sxs-lookup"><span data-stu-id="51aa7-119">RTM\_ENUM\_ALL\_DESTS</span></span>  | <span data-ttu-id="51aa7-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51aa7-120">0x00000000</span></span> | <span data-ttu-id="51aa7-121">Retourne toutes les destinations.</span><span class="sxs-lookup"><span data-stu-id="51aa7-121">Return all destinations.</span></span>                                                                                                                                  |
| <span data-ttu-id="51aa7-122">les \_ \_ propres \_ dest enum RTM</span><span class="sxs-lookup"><span data-stu-id="51aa7-122">RTM\_ENUM\_OWN\_DESTS</span></span>  | <span data-ttu-id="51aa7-123">0x01000000</span><span class="sxs-lookup"><span data-stu-id="51aa7-123">0x01000000</span></span> | <span data-ttu-id="51aa7-124">Retourne uniquement les destinations détenues par le client.</span><span class="sxs-lookup"><span data-stu-id="51aa7-124">Return only those destinations that the client owns.</span></span>                                                                                                      |
| <span data-ttu-id="51aa7-125">\_ \_ tous les \_ itinéraires de l’enum RTM</span><span class="sxs-lookup"><span data-stu-id="51aa7-125">RTM\_ENUM\_ALL\_ROUTES</span></span> | <span data-ttu-id="51aa7-126">0x00000000</span><span class="sxs-lookup"><span data-stu-id="51aa7-126">0x00000000</span></span> | <span data-ttu-id="51aa7-127">Retourne tous les itinéraires.</span><span class="sxs-lookup"><span data-stu-id="51aa7-127">Return all routes.</span></span>                                                                                                                                        |
| <span data-ttu-id="51aa7-128">\_ \_ itinéraires personnalisés de la version RTM \_</span><span class="sxs-lookup"><span data-stu-id="51aa7-128">RTM\_ENUM\_OWN\_ROUTES</span></span> | <span data-ttu-id="51aa7-129">0x00010000</span><span class="sxs-lookup"><span data-stu-id="51aa7-129">0x00010000</span></span> | <span data-ttu-id="51aa7-130">Retourne uniquement les itinéraires détenus par le client.</span><span class="sxs-lookup"><span data-stu-id="51aa7-130">Return only those routes that the client owns.</span></span>                                                                                                            |



 

 

 




