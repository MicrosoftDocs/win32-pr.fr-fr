---
description: Data Flow dans le graphique de filtre
ms.assetid: 3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3
title: Data Flow dans le graphique de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38e0e730dd78e3a42a1121e4a63a053e6016402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846785"
---
# <a name="data-flow-in-the-filter-graph"></a><span data-ttu-id="1fae6-103">Data Flow dans le graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="1fae6-103">Data Flow in the Filter Graph</span></span>

<span data-ttu-id="1fae6-104">Cette section décrit comment les données multimédias se déplacent dans le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="1fae6-104">This section describes how media data moves through the filter graph.</span></span> <span data-ttu-id="1fae6-105">En règle générale, vous n’avez pas besoin de connaître ces détails pour écrire une application DirectShow, bien que dans certaines situations vous pouvez le trouver utile.</span><span class="sxs-lookup"><span data-stu-id="1fae6-105">Usually, you do not need to know these details to write a DirectShow application, although in some situations you may find it helpful.</span></span> <span data-ttu-id="1fae6-106">Si vous écrivez un filtre DirectShow, vous devez comprendre ce document.</span><span class="sxs-lookup"><span data-stu-id="1fae6-106">If you are writing a DirectShow filter, you will need to understand this material.</span></span>

<span data-ttu-id="1fae6-107">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="1fae6-107">This section contains the following topics:</span></span>

-   [<span data-ttu-id="1fae6-108">Vue d’ensemble du Data Flow dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="1fae6-108">Overview of Data Flow in DirectShow</span></span>](overview-of-data-flow-in-directshow.md)
-   [<span data-ttu-id="1fae6-109">Transports</span><span class="sxs-lookup"><span data-stu-id="1fae6-109">Transports</span></span>](transports.md)
-   [<span data-ttu-id="1fae6-110">Exemples et allocators</span><span class="sxs-lookup"><span data-stu-id="1fae6-110">Samples and Allocators</span></span>](samples-and-allocators.md)
-   [<span data-ttu-id="1fae6-111">États de filtre</span><span class="sxs-lookup"><span data-stu-id="1fae6-111">Filter States</span></span>](filter-states.md)
-   [<span data-ttu-id="1fae6-112">Modèle d’extraction</span><span class="sxs-lookup"><span data-stu-id="1fae6-112">Pull Model</span></span>](pull-model.md)

## <a name="related-topics"></a><span data-ttu-id="1fae6-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1fae6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fae6-114">Transmission de données pour les développeurs de filtres</span><span class="sxs-lookup"><span data-stu-id="1fae6-114">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> </dl>

 

 



