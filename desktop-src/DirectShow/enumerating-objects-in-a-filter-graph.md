---
description: Énumération d’objets dans un graphique de filtre
ms.assetid: 04a3dbc8-33c4-4b70-930e-686be2f8301f
title: Énumération d’objets dans un graphique de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369cd3400d3b7fc9944662ed6d32fd67234af90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109106"
---
# <a name="enumerating-objects-in-a-filter-graph"></a><span data-ttu-id="9c715-103">Énumération d’objets dans un graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="9c715-103">Enumerating Objects in a Filter Graph</span></span>

<span data-ttu-id="9c715-104">Une application peut avoir besoin de localiser un filtre particulier dans le graphique de filtre, ou même un code PIN particulier sur un filtre.</span><span class="sxs-lookup"><span data-stu-id="9c715-104">An application might need to locate a particular filter in the filter graph, or even a particular pin on a filter.</span></span> <span data-ttu-id="9c715-105">Par exemple, il peut utiliser une interface exposée par un filtre particulier.</span><span class="sxs-lookup"><span data-stu-id="9c715-105">For example, it might use an interface that a particular filter exposes.</span></span> <span data-ttu-id="9c715-106">Il peut également construire un graphique de filtres spécialisé et avoir besoin d’appeler des méthodes sur des broches individuelles pour connecter les filtres.</span><span class="sxs-lookup"><span data-stu-id="9c715-106">Or, it might construct a specialized filter graph and need to call methods on individual pins to connect the filters.</span></span> <span data-ttu-id="9c715-107">À cet effet, DirectShow offre plusieurs méthodes pour énumérer des objets dans un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="9c715-107">For this purpose, DirectShow provides several methods for enumerating objects in a filter graph.</span></span>

<span data-ttu-id="9c715-108">Les énumérateurs abordés dans cette section suivent le formulaire standard utilisé par les interfaces d’énumération COM.</span><span class="sxs-lookup"><span data-stu-id="9c715-108">The enumerators discussed in this section follow the standard form used by COM enumeration interfaces.</span></span> <span data-ttu-id="9c715-109">Pour plus d’informations, consultez la rubrique « IEnumXXXX » dans le kit de développement logiciel (SDK) de plateforme.</span><span class="sxs-lookup"><span data-stu-id="9c715-109">For more information, see the "IEnumXXXX" topic in the Platform SDK.</span></span> <span data-ttu-id="9c715-110">Pour plus d’informations sur l’énumération des filtres inscrits sur l’ordinateur de l’utilisateur, mais qui ne sont pas encore dans le graphique de filtre, consultez [énumération d’appareils et de filtres](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="9c715-110">For information on enumerating filters that are registered on the user's computer, but aren't yet in the filter graph, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

<span data-ttu-id="9c715-111">Cet article contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="9c715-111">This article contains the following topics:</span></span>

-   [<span data-ttu-id="9c715-112">Énumération des filtres</span><span class="sxs-lookup"><span data-stu-id="9c715-112">Enumerating Filters</span></span>](enumerating-filters.md)
-   [<span data-ttu-id="9c715-113">Énumération des codes confidentiels</span><span class="sxs-lookup"><span data-stu-id="9c715-113">Enumerating Pins</span></span>](enumerating-pins.md)
-   [<span data-ttu-id="9c715-114">Énumération des types de média</span><span class="sxs-lookup"><span data-stu-id="9c715-114">Enumerating Media Types</span></span>](enumerating-media-types.md)

## <a name="related-topics"></a><span data-ttu-id="9c715-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c715-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c715-116">Tâches de base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="9c715-116">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



