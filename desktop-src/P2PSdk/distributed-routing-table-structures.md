---
description: Les structures suivantes prennent en charge les fonctions de l’API de table de routage distribuée (DRT).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Structures de table de routage distribué
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517713"
---
# <a name="distributed-routing-table-structures"></a><span data-ttu-id="76759-103">Structures de table de routage distribué</span><span class="sxs-lookup"><span data-stu-id="76759-103">Distributed Routing Table Structures</span></span>

<span data-ttu-id="76759-104">Les structures suivantes prennent en charge les fonctions de l’API de table de routage distribuée (DRT).</span><span class="sxs-lookup"><span data-stu-id="76759-104">The following structures support the Distributed Routing Table (DRT) API functions.</span></span>



| <span data-ttu-id="76759-105">Structure</span><span class="sxs-lookup"><span data-stu-id="76759-105">Structure</span></span>                                                  | <span data-ttu-id="76759-106">Description</span><span class="sxs-lookup"><span data-stu-id="76759-106">Description</span></span>                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76759-107">**\_données DRT**</span><span class="sxs-lookup"><span data-stu-id="76759-107">**DRT\_DATA**</span></span>](/windows/desktop/api/drt/ns-drt-drt_data)                              | <span data-ttu-id="76759-108">Contient un objet blob de données.</span><span class="sxs-lookup"><span data-stu-id="76759-108">Contains a data blob.</span></span> <span data-ttu-id="76759-109">Cette structure est utilisée par plusieurs fonctions DRT.</span><span class="sxs-lookup"><span data-stu-id="76759-109">This structure is used by several DRT functions.</span></span>                                                                                                                   |
| [<span data-ttu-id="76759-110">**\_inscription DRT**</span><span class="sxs-lookup"><span data-stu-id="76759-110">**DRT\_REGISTRATION**</span></span>](/windows/desktop/api/drt/ns-drt-drt_registration)              | <span data-ttu-id="76759-111">Contient l’enregistrement de la clé.</span><span class="sxs-lookup"><span data-stu-id="76759-111">Contains the key registration.</span></span> <span data-ttu-id="76759-112">Il s’agit d’un membre de la structure de [**\_ \_ résultat de recherche DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) . il s’agit d’un argument passé à [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey).</span><span class="sxs-lookup"><span data-stu-id="76759-112">This is a member of the [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) structure and is an argument passed to [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey).</span></span> |
| [<span data-ttu-id="76759-113">**\_adresse DRT**</span><span class="sxs-lookup"><span data-stu-id="76759-113">**DRT\_ADDRESS**</span></span>](/windows/desktop/api/drt/ns-drt-drt_address)                        | <span data-ttu-id="76759-114">Contient des informations sur le point de terminaison d’un nœud DRT qui a participé à une recherche.</span><span class="sxs-lookup"><span data-stu-id="76759-114">Contains endpoint information about a DRT node that participated in a search.</span></span> <span data-ttu-id="76759-115">Ces informations sont destinées à être utilisées dans le débogage des problèmes de connectivité.</span><span class="sxs-lookup"><span data-stu-id="76759-115">This information is intended for use in debugging connectivity problems.</span></span>                                   |
| [<span data-ttu-id="76759-116">**\_liste d’adresses DRT \_**</span><span class="sxs-lookup"><span data-stu-id="76759-116">**DRT\_ADDRESS\_LIST**</span></span>](/windows/desktop/api/drt/ns-drt-drt_address_list)             | <span data-ttu-id="76759-117">Contient un ensemble de structures d' [**\_ adresses DRT**](/windows/desktop/api/drt/ns-drt-drt_address) représentant les nœuds contactés lors de la recherche d’une clé.</span><span class="sxs-lookup"><span data-stu-id="76759-117">Contains a set of [**DRT\_ADDRESS**](/windows/desktop/api/drt/ns-drt-drt_address) structures representing the nodes contacted during a search for a key.</span></span>                                                             |
| [<span data-ttu-id="76759-118">**\_fournisseur de sécurité DRT \_**</span><span class="sxs-lookup"><span data-stu-id="76759-118">**DRT\_SECURITY\_PROVIDER**</span></span>](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | <span data-ttu-id="76759-119">Définit l’interface qui doit être implémentée par un fournisseur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="76759-119">Defines the interface that must be implemented by a security provider.</span></span>                                                                                                                   |
| [<span data-ttu-id="76759-120">**\_fournisseur de démarrage DRT \_**</span><span class="sxs-lookup"><span data-stu-id="76759-120">**DRT\_BOOTSTRAP\_PROVIDER**</span></span>](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | <span data-ttu-id="76759-121">Définit l’interface qui doit être implémentée par un fournisseur de données d’amorçage.</span><span class="sxs-lookup"><span data-stu-id="76759-121">Defines the interface that must be implemented by a bootstrap provider.</span></span>                                                                                                                  |
| [<span data-ttu-id="76759-122">**\_paramètres DRT**</span><span class="sxs-lookup"><span data-stu-id="76759-122">**DRT\_SETTINGS**</span></span>](/windows/desktop/api/drt/ns-drt-drt_settings)                      | <span data-ttu-id="76759-123">Définit les paramètres DRT à l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="76759-123">Defines DRT settings at initialization.</span></span> <span data-ttu-id="76759-124">Cette structure est passée comme argument à [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).</span><span class="sxs-lookup"><span data-stu-id="76759-124">This structure is passed as an argument to [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).</span></span>                                                                           |
| [<span data-ttu-id="76759-125">**\_informations de recherche DRT \_**</span><span class="sxs-lookup"><span data-stu-id="76759-125">**DRT\_SEARCH\_INFO**</span></span>](/windows/desktop/api/drt/ns-drt-drt_search_info)               | <span data-ttu-id="76759-126">Définit une requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="76759-126">Defines a search query.</span></span> <span data-ttu-id="76759-127">Cette structure est passée comme argument à [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).</span><span class="sxs-lookup"><span data-stu-id="76759-127">This structure is passed as an argument to [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).</span></span>                                                                             |
| [<span data-ttu-id="76759-128">**résultat de la \_ recherche DRT \_**</span><span class="sxs-lookup"><span data-stu-id="76759-128">**DRT\_SEARCH\_RESULT**</span></span>](/windows/desktop/api/drt/ns-drt-drt_search_result)           | <span data-ttu-id="76759-129">Contient un résultat de recherche.</span><span class="sxs-lookup"><span data-stu-id="76759-129">Contains a search result.</span></span> <span data-ttu-id="76759-130">Cette structure est retournée par [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).</span><span class="sxs-lookup"><span data-stu-id="76759-130">This structure is returned by [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).</span></span>                                                                                |
| [<span data-ttu-id="76759-131">**\_données d’événement DRT \_**</span><span class="sxs-lookup"><span data-stu-id="76759-131">**DRT\_EVENT\_DATA**</span></span>](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | <span data-ttu-id="76759-132">Contient les données d’événement retournées par l’appel de [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) après qu’une application a reçu un signal d’événement.</span><span class="sxs-lookup"><span data-stu-id="76759-132">Contains the event data returned by calling [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) after an application receives an event signal.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="76759-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="76759-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76759-134">Énumérations de tables de routage distribuées</span><span class="sxs-lookup"><span data-stu-id="76759-134">Distributed Routing Table Enumerations</span></span>](distributed-routing-table-enumerations.md)
</dt> <dt>

[<span data-ttu-id="76759-135">Fonctions de table de routage distribuée</span><span class="sxs-lookup"><span data-stu-id="76759-135">Distributed Routing Table Functions</span></span>](distributed-routing-table-functions.md)
</dt> <dt>

[<span data-ttu-id="76759-136">Référence de API Table de routage distribué</span><span class="sxs-lookup"><span data-stu-id="76759-136">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



