---
description: Les énumérations suivantes prennent en charge l’API de table de routage distribuée (DRT).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Énumérations de tables de routage distribuées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c432b156a9299a9f70026a394a6fd97f06528a25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519905"
---
# <a name="distributed-routing-table-enumerations"></a><span data-ttu-id="82c98-103">Énumérations de tables de routage distribuées</span><span class="sxs-lookup"><span data-stu-id="82c98-103">Distributed Routing Table Enumerations</span></span>

<span data-ttu-id="82c98-104">Les énumérations suivantes prennent en charge l’API de table de routage distribuée (DRT).</span><span class="sxs-lookup"><span data-stu-id="82c98-104">The following enumerations support the Distributed Routing Table (DRT) API.</span></span>



| <span data-ttu-id="82c98-105">Énumération</span><span class="sxs-lookup"><span data-stu-id="82c98-105">Enumeration</span></span>                                                            | <span data-ttu-id="82c98-106">Description</span><span class="sxs-lookup"><span data-stu-id="82c98-106">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82c98-107">**\_étendue DRT**</span><span class="sxs-lookup"><span data-stu-id="82c98-107">**DRT\_SCOPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | <span data-ttu-id="82c98-108">Définit le jeu d’étendues IPv6 dans lequel DRT fonctionne lors de l’utilisation du transport UDP IPv6 créé par [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport).</span><span class="sxs-lookup"><span data-stu-id="82c98-108">Defines the set of IPv6 scopes in which DRT will operate when using the IPv6 UDP transport created by [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport).</span></span> |
| [<span data-ttu-id="82c98-109">**\_indicateurs d’adresse DRT \_**</span><span class="sxs-lookup"><span data-stu-id="82c98-109">**DRT\_ADDRESS\_FLAGS**</span></span>](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | <span data-ttu-id="82c98-110">Définit l’ensemble des réponses qui peuvent être retournées par un nœud intermédiaire lors de l’exécution d’une recherche de clé.</span><span class="sxs-lookup"><span data-stu-id="82c98-110">Defines the set of responses that may be returned by an intermediate node when performing a search for a key.</span></span>                                                         |
| [<span data-ttu-id="82c98-111">**\_État DRT**</span><span class="sxs-lookup"><span data-stu-id="82c98-111">**DRT\_STATUS**</span></span>](/windows/desktop/api/drt/ne-drt-drt_status)                                      | <span data-ttu-id="82c98-112">Définit la connectivité possible et les États d’erreur d’un nœud local.</span><span class="sxs-lookup"><span data-stu-id="82c98-112">Defines the possible connectivity and error states of a local node.</span></span>                                                                                                   |
| [<span data-ttu-id="82c98-113">**\_type de correspondance DRT \_**</span><span class="sxs-lookup"><span data-stu-id="82c98-113">**DRT\_MATCH\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | <span data-ttu-id="82c98-114">Définit l’exactitude des résultats retournés lorsqu’une recherche est effectuée.</span><span class="sxs-lookup"><span data-stu-id="82c98-114">Defines the exactness of results returned when a search is performed.</span></span>                                                                                                 |
| [<span data-ttu-id="82c98-115">**\_type de \_ modification de clé DRT LEAFSET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="82c98-115">**DRT\_LEAFSET\_KEY\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | <span data-ttu-id="82c98-116">Définit l’ensemble des types de modifications qui peuvent être exécutés sur un nœud de groupe feuille local dans le cache DRT local.</span><span class="sxs-lookup"><span data-stu-id="82c98-116">Defines the set of change types that can be performed on a local leaf set node in the local DRT cache.</span></span>                                                                |
| [<span data-ttu-id="82c98-117">**\_type d’événement DRT \_**</span><span class="sxs-lookup"><span data-stu-id="82c98-117">**DRT\_EVENT\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | <span data-ttu-id="82c98-118">Définit l’ensemble des événements qui peuvent être déclenchés par le DRT.</span><span class="sxs-lookup"><span data-stu-id="82c98-118">Defines the set of events that can be raised by the DRT.</span></span>                                                                                                              |
| [<span data-ttu-id="82c98-119">**\_mode de sécurité DRT \_**</span><span class="sxs-lookup"><span data-stu-id="82c98-119">**DRT\_SECURITY\_MODE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | <span data-ttu-id="82c98-120">Définit les modes de sécurité possibles de l’DRT.</span><span class="sxs-lookup"><span data-stu-id="82c98-120">Defines the possible security modes of the DRT.</span></span> <span data-ttu-id="82c98-121">Cette énumération est un champ de la structure de [**\_ paramètres DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .</span><span class="sxs-lookup"><span data-stu-id="82c98-121">This enumeration is a field of the [**DRT\_SETTINGS**](/windows/desktop/api/drt/ns-drt-drt_settings) structure.</span></span>                                   |
| [<span data-ttu-id="82c98-122">**\_État de l’inscription DRT \_**</span><span class="sxs-lookup"><span data-stu-id="82c98-122">**DRT\_REGISTRATION\_STATE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | <span data-ttu-id="82c98-123">Définit l’état d’une clé inscrite.</span><span class="sxs-lookup"><span data-stu-id="82c98-123">Defines the state of a registered key.</span></span>                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="82c98-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="82c98-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82c98-125">Structures de table de routage distribué</span><span class="sxs-lookup"><span data-stu-id="82c98-125">Distributed Routing Table Structures</span></span>](distributed-routing-table-structures.md)
</dt> <dt>

[<span data-ttu-id="82c98-126">Fonctions de table de routage distribuée</span><span class="sxs-lookup"><span data-stu-id="82c98-126">Distributed Routing Table Functions</span></span>](distributed-routing-table-functions.md)
</dt> <dt>

[<span data-ttu-id="82c98-127">Référence de API Table de routage distribué</span><span class="sxs-lookup"><span data-stu-id="82c98-127">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



