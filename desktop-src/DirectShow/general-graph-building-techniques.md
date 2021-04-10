---
description: Techniques d' Graph-Building générales
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: Techniques d' Graph-Building générales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200663"
---
# <a name="general-graph-building-techniques"></a><span data-ttu-id="27c0d-103">Techniques d' Graph-Building générales</span><span class="sxs-lookup"><span data-stu-id="27c0d-103">General Graph-Building Techniques</span></span>

<span data-ttu-id="27c0d-104">Chaque application DirectShow démarre en générant un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="27c0d-104">Every DirectShow application starts by building a filter graph.</span></span> <span data-ttu-id="27c0d-105">À mesure que vous lisez les rubriques de vue d’ensemble de la documentation DirectShow, vous constaterez que la plupart commencent par décrire le type de graphique de filtre dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="27c0d-105">As you read the overview topics in the DirectShow documentation, you will find that most start by describing what kind of filter graph you need.</span></span> <span data-ttu-id="27c0d-106">Dans certains cas, il existe une méthode ou un objet d’assistance spécifiquement conçu pour créer ce type de graphique.</span><span class="sxs-lookup"><span data-stu-id="27c0d-106">In some cases, there is a method or a helper object specifically designed for building that type of graph.</span></span> <span data-ttu-id="27c0d-107">Par exemple, l’objet [DVD Graph Builder](dvd-graph-builder.md) crée des graphiques de lecture DVD.</span><span class="sxs-lookup"><span data-stu-id="27c0d-107">For example, the [DVD Graph Builder](dvd-graph-builder.md) object builds DVD playback graphs.</span></span> <span data-ttu-id="27c0d-108">Dans d’autres cas, l’application doit construire le graphique en ajoutant des filtres et en les connectant.</span><span class="sxs-lookup"><span data-stu-id="27c0d-108">In other cases, the application must construct the graph by adding filters and connecting them.</span></span>

<span data-ttu-id="27c0d-109">Cette section présente des fonctions d’assistance qui implémentent des opérations de création de graphiques de base.</span><span class="sxs-lookup"><span data-stu-id="27c0d-109">This section presents some helper functions that implement basic graph-building operations.</span></span> <span data-ttu-id="27c0d-110">Elles peuvent être utilisées par n’importe quelle application DirectShow qui doit générer ou modifier un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="27c0d-110">They can be used by any DirectShow application that needs to build or modify a filter graph.</span></span> <span data-ttu-id="27c0d-111">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="27c0d-111">This section contains the following topics:</span></span>

-   [<span data-ttu-id="27c0d-112">Ajouter un filtre par CLSID</span><span class="sxs-lookup"><span data-stu-id="27c0d-112">Add a Filter by CLSID</span></span>](add-a-filter-by-clsid.md)
-   [<span data-ttu-id="27c0d-113">Rechercher un code confidentiel non connecté sur un filtre</span><span class="sxs-lookup"><span data-stu-id="27c0d-113">Find an Unconnected Pin on a Filter</span></span>](find-an-unconnected-pin-on-a-filter.md)
-   [<span data-ttu-id="27c0d-114">Connecter deux filtres</span><span class="sxs-lookup"><span data-stu-id="27c0d-114">Connect Two Filters</span></span>](connect-two-filters.md)
-   [<span data-ttu-id="27c0d-115">Rechercher une interface sur un filtre ou un code PIN</span><span class="sxs-lookup"><span data-stu-id="27c0d-115">Find an Interface on a Filter or Pin</span></span>](find-an-interface-on-a-filter-or-pin.md)
-   [<span data-ttu-id="27c0d-116">Rechercher l’homologue d’un filtre</span><span class="sxs-lookup"><span data-stu-id="27c0d-116">Find a Filter's Peer</span></span>](find-a-filters-peer.md)
-   [<span data-ttu-id="27c0d-117">Supprimer tous les filtres dans le graphique</span><span class="sxs-lookup"><span data-stu-id="27c0d-117">Remove All the Filters in the Graph</span></span>](remove-all-the-filters-in-the-graph.md)
-   [<span data-ttu-id="27c0d-118">Création de graphiques à l’aide du générateur de graphiques de capture</span><span class="sxs-lookup"><span data-stu-id="27c0d-118">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a><span data-ttu-id="27c0d-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27c0d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27c0d-120">Tâches de base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="27c0d-120">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="27c0d-121">Énumération des appareils et des filtres</span><span class="sxs-lookup"><span data-stu-id="27c0d-121">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="27c0d-122">Énumération d’objets dans un graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="27c0d-122">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="27c0d-123">Connexion intelligente</span><span class="sxs-lookup"><span data-stu-id="27c0d-123">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 



