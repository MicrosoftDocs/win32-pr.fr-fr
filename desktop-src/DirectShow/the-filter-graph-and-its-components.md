---
description: Le graphique de filtre et ses composants
ms.assetid: 3747bfcd-1e4a-404c-a493-26d3c20bab21
title: Le graphique de filtre et ses composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473fb3dfe327eb43bb2065417c7be80f7537d06a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521328"
---
# <a name="the-filter-graph-and-its-components"></a><span data-ttu-id="cf78f-103">Le graphique de filtre et ses composants</span><span class="sxs-lookup"><span data-stu-id="cf78f-103">The Filter Graph and Its Components</span></span>

<span data-ttu-id="cf78f-104">Cet article décrit les principaux composants de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cf78f-104">This article describes the major components of DirectShow.</span></span> <span data-ttu-id="cf78f-105">Il s’adresse aux développeurs d’applications et aux développeurs qui écrivent des filtres DirectShow personnalisés.</span><span class="sxs-lookup"><span data-stu-id="cf78f-105">It is intended as an introduction for application developers and for developers writing custom DirectShow filters.</span></span> <span data-ttu-id="cf78f-106">Les développeurs d’applications peuvent généralement ignorer un grand nombre des détails de bas niveau de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cf78f-106">Application developers can usually ignore many of the low-level details of DirectShow.</span></span> <span data-ttu-id="cf78f-107">Toutefois, il est toujours judicieux de lire cette section pour avoir une compréhension générale de l’architecture DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cf78f-107">However, it is still a good idea to read this section, to have a general understanding of the DirectShow architecture.</span></span>

<span data-ttu-id="cf78f-108">Cet article contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf78f-108">This article contains the following sections:</span></span>

-   [<span data-ttu-id="cf78f-109">À propos des filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="cf78f-109">About DirectShow Filters</span></span>](about-directshow-filters.md)
-   [<span data-ttu-id="cf78f-110">À propos du gestionnaire de graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="cf78f-110">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)
-   [<span data-ttu-id="cf78f-111">À propos des types de média</span><span class="sxs-lookup"><span data-stu-id="cf78f-111">About Media Types</span></span>](about-media-types.md)
-   [<span data-ttu-id="cf78f-112">À propos des exemples de supports et des allocators</span><span class="sxs-lookup"><span data-stu-id="cf78f-112">About Media Samples and Allocators</span></span>](about-media-samples-and-allocators.md)
-   [<span data-ttu-id="cf78f-113">Comment les périphériques matériels participent au graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="cf78f-113">How Hardware Devices Participate in the Filter Graph</span></span>](how-hardware-devices-participate-in-the-filter-graph.md)

 

 



