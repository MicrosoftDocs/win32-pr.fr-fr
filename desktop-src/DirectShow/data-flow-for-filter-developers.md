---
description: Transmission de données pour les développeurs de filtres
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Transmission de données pour les développeurs de filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb4e4123e8617190a459ff500d1100c0dbbb8ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033550"
---
# <a name="data-flow-for-filter-developers"></a><span data-ttu-id="763c3-103">Transmission de données pour les développeurs de filtres</span><span class="sxs-lookup"><span data-stu-id="763c3-103">Data Flow for Filter Developers</span></span>

<span data-ttu-id="763c3-104">Cette section décrit en détail la façon dont les données se déplacent dans le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="763c3-104">This section describes in detail how data moves through the filter graph.</span></span> <span data-ttu-id="763c3-105">Il se concentre sur le transport de mémoire local à l’aide de l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) ou [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="763c3-105">It focuses on local memory transport using the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) or [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="763c3-106">Elle est destinée aux développeurs qui écrivent leurs propres filtres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="763c3-106">It is intended for developers who are writing their own custom filters.</span></span> <span data-ttu-id="763c3-107">Pour obtenir une présentation générale de la façon dont Microsoft DirectShow gère le workflow de données, consultez [Data Flow dans le graphique de filtre](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="763c3-107">For a general introduction to how Microsoft DirectShow handles data flow, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="763c3-108">Un grand nombre de données se déplacent dans un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="763c3-108">A lot of data moves through a filter graph.</span></span> <span data-ttu-id="763c3-109">Il se divise en deux catégories : données de média et données de contrôle.</span><span class="sxs-lookup"><span data-stu-id="763c3-109">It falls roughly into two categories: media data and control data.</span></span> <span data-ttu-id="763c3-110">En général, les données multimédia transitent en aval et contrôlent les flux de données en amont.</span><span class="sxs-lookup"><span data-stu-id="763c3-110">In general, media data travels downstream and control data travels upstream.</span></span> <span data-ttu-id="763c3-111">Les données multimédias incluent les images vidéo, les échantillons audio, les paquets MPEG, etc. qui composent un flux, mais également les commandes de vidage, les notifications de fin de flux et les autres données qui transitent par le flux.</span><span class="sxs-lookup"><span data-stu-id="763c3-111">Media data includes the video frames, audio samples, MPEG packets, and so forth that make up a stream, but also includes flush commands, end-of-stream notifications, and other data that travels with the stream.</span></span> <span data-ttu-id="763c3-112">Les données de contrôle ne font pas partie du flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="763c3-112">Control data is not part of the media stream.</span></span> <span data-ttu-id="763c3-113">Les requêtes de contrôle qualité et les commandes de recherche sont des exemples de données de contrôle.</span><span class="sxs-lookup"><span data-stu-id="763c3-113">Examples of control data are quality-control requests and seek commands.</span></span>

<span data-ttu-id="763c3-114">Cette section contient les articles suivants.</span><span class="sxs-lookup"><span data-stu-id="763c3-114">This section contains the following articles.</span></span>

-   [<span data-ttu-id="763c3-115">Exemples de livrables</span><span class="sxs-lookup"><span data-stu-id="763c3-115">Delivering Samples</span></span>](delivering-samples.md)
-   [<span data-ttu-id="763c3-116">Traitement des données</span><span class="sxs-lookup"><span data-stu-id="763c3-116">Processing Data</span></span>](processing-data.md)
-   [<span data-ttu-id="763c3-117">Notifications de fin de flux</span><span class="sxs-lookup"><span data-stu-id="763c3-117">End-of-Stream Notifications</span></span>](end-of-stream-notifications.md)
-   [<span data-ttu-id="763c3-118">Nouveaux segments</span><span class="sxs-lookup"><span data-stu-id="763c3-118">New Segments</span></span>](new-segments.md)
-   [<span data-ttu-id="763c3-119">Vidage</span><span class="sxs-lookup"><span data-stu-id="763c3-119">Flushing</span></span>](flushing.md)
-   [<span data-ttu-id="763c3-120">Cherche</span><span class="sxs-lookup"><span data-stu-id="763c3-120">Seeking</span></span>](seeking.md)
-   [<span data-ttu-id="763c3-121">Modifications de format dynamique</span><span class="sxs-lookup"><span data-stu-id="763c3-121">Dynamic Format Changes</span></span>](dynamic-format-changes.md)

## <a name="related-topics"></a><span data-ttu-id="763c3-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="763c3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="763c3-123">Gestion du contrôle de la qualité</span><span class="sxs-lookup"><span data-stu-id="763c3-123">Quality-Control Management</span></span>](quality-control-management.md)
</dt> <dt>

[<span data-ttu-id="763c3-124">Threads et sections critiques</span><span class="sxs-lookup"><span data-stu-id="763c3-124">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> <dt>

[<span data-ttu-id="763c3-125">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="763c3-125">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



