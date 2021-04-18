---
title: Indicateurs d’affichage
description: Utilisez les indicateurs d’affichage pour contrôler les vues de table de routage.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5192bf3e1acaa91412d8ae7e06d035e54af1ece6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509407"
---
# <a name="view-flags"></a><span data-ttu-id="890cf-103">Indicateurs d’affichage</span><span class="sxs-lookup"><span data-stu-id="890cf-103">View Flags</span></span>

<span data-ttu-id="890cf-104">Utilisez les indicateurs d’affichage pour contrôler les vues de table de routage.</span><span class="sxs-lookup"><span data-stu-id="890cf-104">Use the View Flags to control routing table views.</span></span>



| <span data-ttu-id="890cf-105">Constante</span><span class="sxs-lookup"><span data-stu-id="890cf-105">Constant</span></span>                 | <span data-ttu-id="890cf-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="890cf-106">Value</span></span>      | <span data-ttu-id="890cf-107">Description</span><span class="sxs-lookup"><span data-stu-id="890cf-107">Description</span></span>                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| <span data-ttu-id="890cf-108">\_taille maximale de l' \_ adresse RTM \_</span><span class="sxs-lookup"><span data-stu-id="890cf-108">RTM\_MAX \_ADDRESS\_SIZE</span></span> | <span data-ttu-id="890cf-109">16</span><span class="sxs-lookup"><span data-stu-id="890cf-109">16</span></span>         | <span data-ttu-id="890cf-110">Taille maximale d’adresse pour une famille d’adresses.</span><span class="sxs-lookup"><span data-stu-id="890cf-110">Max address size for an address family.</span></span>                          |
| <span data-ttu-id="890cf-111">\_vues maximales RTM \_</span><span class="sxs-lookup"><span data-stu-id="890cf-111">RTM\_MAX\_VIEWS</span></span>          | <span data-ttu-id="890cf-112">32</span><span class="sxs-lookup"><span data-stu-id="890cf-112">32</span></span>         | <span data-ttu-id="890cf-113">Nombre maximal de vues qui peuvent être actives dans la table de routage.</span><span class="sxs-lookup"><span data-stu-id="890cf-113">Maximum number of views that can be active in the routing table.</span></span> |
| <span data-ttu-id="890cf-114">\_ID de vue RTM \_ \_ UCAST</span><span class="sxs-lookup"><span data-stu-id="890cf-114">RTM\_VIEW\_ID\_UCAST</span></span>     | <span data-ttu-id="890cf-115">0</span><span class="sxs-lookup"><span data-stu-id="890cf-115">0</span></span>          | <span data-ttu-id="890cf-116">Spécifie une vue de monodiffusion.</span><span class="sxs-lookup"><span data-stu-id="890cf-116">Specifies a unicast view.</span></span>                                        |
| <span data-ttu-id="890cf-117">\_ID de vue RTM \_ \_ mcast</span><span class="sxs-lookup"><span data-stu-id="890cf-117">RTM\_VIEW\_ID\_MCAST</span></span>     | <span data-ttu-id="890cf-118">1</span><span class="sxs-lookup"><span data-stu-id="890cf-118">1</span></span>          | <span data-ttu-id="890cf-119">Spécifie une vue de multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="890cf-119">Specifies a multicast view.</span></span>                                      |
| <span data-ttu-id="890cf-120">\_taille du \_ masque de vue RTM \_</span><span class="sxs-lookup"><span data-stu-id="890cf-120">RTM\_VIEW\_MASK\_SIZE</span></span>    | <span data-ttu-id="890cf-121">0x20</span><span class="sxs-lookup"><span data-stu-id="890cf-121">0x20</span></span>       | <span data-ttu-id="890cf-122">Spécifie le nombre maximal de vues qui peuvent être configurées.</span><span class="sxs-lookup"><span data-stu-id="890cf-122">Specifies the maximum number of views that can be configured.</span></span>    |
| <span data-ttu-id="890cf-123">\_masque de vue RTM \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="890cf-123">RTM\_VIEW\_MASK\_NONE</span></span>    | <span data-ttu-id="890cf-124">0x00000000</span><span class="sxs-lookup"><span data-stu-id="890cf-124">0x00000000</span></span> | <span data-ttu-id="890cf-125">Retourne les informations indépendamment de la vue.</span><span class="sxs-lookup"><span data-stu-id="890cf-125">Returns information regardless of the view.</span></span>                      |
| <span data-ttu-id="890cf-126">\_ \_ masque de vue RTM \_ any</span><span class="sxs-lookup"><span data-stu-id="890cf-126">RTM\_VIEW\_MASK\_ANY</span></span>     | <span data-ttu-id="890cf-127">0x00000000</span><span class="sxs-lookup"><span data-stu-id="890cf-127">0x00000000</span></span> | <span data-ttu-id="890cf-128">Retourne les destinations de toutes les vues.</span><span class="sxs-lookup"><span data-stu-id="890cf-128">Returns destinations from all views.</span></span> <span data-ttu-id="890cf-129">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="890cf-129">This is the default value.</span></span>  |
| <span data-ttu-id="890cf-130">\_masque de vue RTM \_ \_ UCAST</span><span class="sxs-lookup"><span data-stu-id="890cf-130">RTM\_VIEW\_MASK\_UCAST</span></span>   | <span data-ttu-id="890cf-131">0x00000001</span><span class="sxs-lookup"><span data-stu-id="890cf-131">0x00000001</span></span> | <span data-ttu-id="890cf-132">Retourne les destinations de la vue monodiffusion.</span><span class="sxs-lookup"><span data-stu-id="890cf-132">Returns destinations from the unicast view.</span></span>                      |
| <span data-ttu-id="890cf-133">\_masque de vue RTM \_ \_ mcast</span><span class="sxs-lookup"><span data-stu-id="890cf-133">RTM\_VIEW\_MASK\_MCAST</span></span>   | <span data-ttu-id="890cf-134">0x00000002</span><span class="sxs-lookup"><span data-stu-id="890cf-134">0x00000002</span></span> | <span data-ttu-id="890cf-135">Retourne les destinations de la vue multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="890cf-135">Returns destinations from the multicast view.</span></span>                    |
| <span data-ttu-id="890cf-136">affichage RTM- \_ \_ Masquer \_ tout</span><span class="sxs-lookup"><span data-stu-id="890cf-136">RTM\_VIEW\_MASK\_ALL</span></span>     | <span data-ttu-id="890cf-137">Égale</span><span class="sxs-lookup"><span data-stu-id="890cf-137">0xFFFFFFFF</span></span> | <span data-ttu-id="890cf-138">Retourne des informations de toutes les vues.</span><span class="sxs-lookup"><span data-stu-id="890cf-138">Returns information from all views.</span></span>                              |



 

 

 




