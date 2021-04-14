---
description: Simulation de la génération de graphiques avec GraphEdit
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: Simulation de la génération de graphiques avec GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76878997c873c74d454979ccda689a9c241489d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481968"
---
# <a name="simulating-graph-building-with-graphedit"></a><span data-ttu-id="95445-103">Simulation de la génération de graphiques avec GraphEdit</span><span class="sxs-lookup"><span data-stu-id="95445-103">Simulating Graph Building with GraphEdit</span></span>

<span data-ttu-id="95445-104">DirectShow fournit un utilitaire de débogage appelé GraphEdit, que vous pouvez utiliser pour créer et tester des graphiques de filtre.</span><span class="sxs-lookup"><span data-stu-id="95445-104">DirectShow provides a debugging utility called GraphEdit, which you can use to create and test filter graphs.</span></span>

<span data-ttu-id="95445-105">GraphEdit est un outil visuel permettant de créer des graphiques de filtres.</span><span class="sxs-lookup"><span data-stu-id="95445-105">GraphEdit is a visual tool for building filter graphs.</span></span> <span data-ttu-id="95445-106">Avec GraphEdit, vous pouvez expérimenter avec un graphique de filtre avant d’écrire du code d’application.</span><span class="sxs-lookup"><span data-stu-id="95445-106">With GraphEdit, you can experiment with a filter graph before you write any application code.</span></span> <span data-ttu-id="95445-107">Vous pouvez également charger un graphique de filtre créé par votre application pour vérifier que votre application génère le graphique approprié.</span><span class="sxs-lookup"><span data-stu-id="95445-107">You can also load a filter graph that your application creates, to verify that your application is building the correct graph.</span></span> <span data-ttu-id="95445-108">Si vous développez un filtre personnalisé, GraphEdit offre un moyen rapide de le tester : Chargez simplement un graphique avec votre filtre personnalisé et essayez d’exécuter le graphique.</span><span class="sxs-lookup"><span data-stu-id="95445-108">If you develop a custom filter, GraphEdit provides a quick way to test it: Simply load a graph with your custom filter and try running the graph.</span></span> <span data-ttu-id="95445-109">Si vous débutez avec DirectShow, GraphEdit est un bon moyen de vous familiariser avec les graphiques de filtres et l’architecture DirectShow.</span><span class="sxs-lookup"><span data-stu-id="95445-109">If you are new to DirectShow, GraphEdit is a good way to become familiar with filter graphs and the DirectShow architecture.</span></span>

<span data-ttu-id="95445-110">L’illustration suivante montre comment GraphEdit représente un graphique de filtre simple.</span><span class="sxs-lookup"><span data-stu-id="95445-110">The following illustration shows how GraphEdit represents a simple filter graph.</span></span>

![graphique de filtre simple dans GraphEdit](images/gedit09.png)

<span data-ttu-id="95445-112">Chaque filtre est représenté sous la forme d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="95445-112">Each filter is represented as a rectangle.</span></span> <span data-ttu-id="95445-113">Les petits carrés situés le long des bords des filtres représentent des broches.</span><span class="sxs-lookup"><span data-stu-id="95445-113">Smaller squares along the edges of the filters represent pins.</span></span> <span data-ttu-id="95445-114">Les broches d’entrée se trouvent sur le côté gauche du filtre et les broches de sortie se trouvent sur le côté droit.</span><span class="sxs-lookup"><span data-stu-id="95445-114">Input pins are on the left side of the filter, and output pins are on the right side.</span></span> <span data-ttu-id="95445-115">Les flèches représentent les connexions entre les broches.</span><span class="sxs-lookup"><span data-stu-id="95445-115">The arrows represent the connections between pins.</span></span>

<span data-ttu-id="95445-116">Avec GraphEdit, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="95445-116">With GraphEdit, you can:</span></span>

-   <span data-ttu-id="95445-117">Créez et modifiez des graphiques de filtre à l’aide d’une interface de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="95445-117">Create and modify filter graphs using a visual, drag-and-drop interface.</span></span>
-   <span data-ttu-id="95445-118">Simulez des appels de programmation pour générer un graphique.</span><span class="sxs-lookup"><span data-stu-id="95445-118">Simulate programmatic calls to build a graph.</span></span>
-   <span data-ttu-id="95445-119">Exécuter, suspendre, arrêter et Rechercher un graphique.</span><span class="sxs-lookup"><span data-stu-id="95445-119">Run, pause, stop, and seek a graph.</span></span>
-   <span data-ttu-id="95445-120">Consultez les filtres qui sont inscrits sur votre ordinateur et affichez les informations de Registre pour chaque filtre.</span><span class="sxs-lookup"><span data-stu-id="95445-120">See what filters are registered on your computer, and view registry information for each filter.</span></span>
-   <span data-ttu-id="95445-121">Affichez les pages de propriétés de filtre.</span><span class="sxs-lookup"><span data-stu-id="95445-121">View filter property pages.</span></span>
-   <span data-ttu-id="95445-122">Affichez les types de médias des connexions de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="95445-122">View the media types of pin connections.</span></span>

<span data-ttu-id="95445-123">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="95445-123">This section contains the following topics:</span></span>

-   [<span data-ttu-id="95445-124">Utilisation de GraphEdit</span><span class="sxs-lookup"><span data-stu-id="95445-124">Using GraphEdit</span></span>](using-graphedit.md)
-   [<span data-ttu-id="95445-125">Chargement d’un graphique à partir d’un processus externe</span><span class="sxs-lookup"><span data-stu-id="95445-125">Loading a Graph From an External Process</span></span>](loading-a-graph-from-an-external-process.md)
-   [<span data-ttu-id="95445-126">Enregistrement d’un graphique de filtre dans un fichier baGraphEdit</span><span class="sxs-lookup"><span data-stu-id="95445-126">Saving a Filter Graph to a GraphEdit File</span></span>](saving-a-filter-graph-to-a-graphedit-file.md)
-   [<span data-ttu-id="95445-127">Chargement d’un fichier baGraphEdit par programmation</span><span class="sxs-lookup"><span data-stu-id="95445-127">Loading a GraphEdit File Programmatically</span></span>](loading-a-graphedit-file-programmatically.md)
-   [<span data-ttu-id="95445-128">Format de fichier GraphEdit</span><span class="sxs-lookup"><span data-stu-id="95445-128">GraphEdit File Format</span></span>](graphedit-file-format.md)

## <a name="related-topics"></a><span data-ttu-id="95445-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95445-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95445-130">Utilisation de DirectShow</span><span class="sxs-lookup"><span data-stu-id="95445-130">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



