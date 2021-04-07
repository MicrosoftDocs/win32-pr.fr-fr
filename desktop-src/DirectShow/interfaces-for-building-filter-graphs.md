---
description: Interfaces pour la création de graphiques de filtre
ms.assetid: 18d5217a-7f4e-49e9-ac14-2f4ba229e065
title: Interfaces pour la création de graphiques de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862d581f44a711cc6f2aa094210571995b15005b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746012"
---
# <a name="interfaces-for-building-filter-graphs"></a><span data-ttu-id="6e6be-103">Interfaces pour la création de graphiques de filtre</span><span class="sxs-lookup"><span data-stu-id="6e6be-103">Interfaces for Building Filter Graphs</span></span>

<span data-ttu-id="6e6be-104">Les applications utilisent ces interfaces pour générer différents types de graphiques de filtre.</span><span class="sxs-lookup"><span data-stu-id="6e6be-104">Applications use these interfaces to build various types of filter graphs.</span></span>



| <span data-ttu-id="6e6be-105">Interface</span><span class="sxs-lookup"><span data-stu-id="6e6be-105">Interface</span></span>                                                  | <span data-ttu-id="6e6be-106">Description</span><span class="sxs-lookup"><span data-stu-id="6e6be-106">Description</span></span>                                                 |
|------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="6e6be-107">**IAMFilterGraphCallback**</span><span class="sxs-lookup"><span data-stu-id="6e6be-107">**IAMFilterGraphCallback**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback)   | <span data-ttu-id="6e6be-108">Recevoir des notifications de rappel si un code confidentiel ne peut pas être rendu.</span><span class="sxs-lookup"><span data-stu-id="6e6be-108">Receive callback notifications if a pin cannot be rendered.</span></span> |
| [<span data-ttu-id="6e6be-109">**IAMGraphBuilderCallback**</span><span class="sxs-lookup"><span data-stu-id="6e6be-109">**IAMGraphBuilderCallback**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) | <span data-ttu-id="6e6be-110">Fournit un mécanisme de rappel lors de la génération du graphique.</span><span class="sxs-lookup"><span data-stu-id="6e6be-110">Provides a callback mechanism during graph building.</span></span>        |
| [<span data-ttu-id="6e6be-111">**ICaptureGraphBuilder2**</span><span class="sxs-lookup"><span data-stu-id="6e6be-111">**ICaptureGraphBuilder2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)     | <span data-ttu-id="6e6be-112">Créer des graphiques de filtre pour la capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="6e6be-112">Build filter graphs for video capture.</span></span>                      |
| [<span data-ttu-id="6e6be-113">**ICreateDevEnum**</span><span class="sxs-lookup"><span data-stu-id="6e6be-113">**ICreateDevEnum**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)                   | <span data-ttu-id="6e6be-114">Énumérer les périphériques système, tels que les périphériques de capture.</span><span class="sxs-lookup"><span data-stu-id="6e6be-114">Enumerate system devices, such as capture devices.</span></span>          |
| [<span data-ttu-id="6e6be-115">**IDvdGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="6e6be-115">**IDvdGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)               | <span data-ttu-id="6e6be-116">Générez des graphiques de filtre pour la navigation et la lecture des DVD.</span><span class="sxs-lookup"><span data-stu-id="6e6be-116">Build filter graphs for DVD navigation and playback.</span></span>        |
| [<span data-ttu-id="6e6be-117">**IEnumFilters**</span><span class="sxs-lookup"><span data-stu-id="6e6be-117">**IEnumFilters**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)                       | <span data-ttu-id="6e6be-118">Énumérez les filtres dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="6e6be-118">Enumerate the filters in the graph.</span></span>                         |
| [<span data-ttu-id="6e6be-119">**IFilterGraph2**</span><span class="sxs-lookup"><span data-stu-id="6e6be-119">**IFilterGraph2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)                     | <span data-ttu-id="6e6be-120">Ajoutez, supprimez ou connectez des filtres.</span><span class="sxs-lookup"><span data-stu-id="6e6be-120">Add, remove, or connect filters.</span></span>                            |
| [<span data-ttu-id="6e6be-121">**IFilterMapper2**</span><span class="sxs-lookup"><span data-stu-id="6e6be-121">**IFilterMapper2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)                   | <span data-ttu-id="6e6be-122">Énumérer les filtres inscrits sur le système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6e6be-122">Enumerate the filters registered on the user's system.</span></span>      |
| [<span data-ttu-id="6e6be-123">**IGraphBuilder**</span><span class="sxs-lookup"><span data-stu-id="6e6be-123">**IGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)                     | <span data-ttu-id="6e6be-124">Générez des graphiques de filtre pour la lecture de fichiers ou pour des utilisations personnalisées.</span><span class="sxs-lookup"><span data-stu-id="6e6be-124">Build filter graphs for file playback or for custom uses.</span></span>   |
| [<span data-ttu-id="6e6be-125">**IGraphConfig**</span><span class="sxs-lookup"><span data-stu-id="6e6be-125">**IGraphConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)                       | <span data-ttu-id="6e6be-126">Reconfigurez dynamiquement un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="6e6be-126">Dynamically reconfigure a filter graph.</span></span>                     |
| [<span data-ttu-id="6e6be-127">**IGraphVersion**</span><span class="sxs-lookup"><span data-stu-id="6e6be-127">**IGraphVersion**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphversion)                     | <span data-ttu-id="6e6be-128">Déterminez le moment où le graphique change.</span><span class="sxs-lookup"><span data-stu-id="6e6be-128">Determine when the graph changes.</span></span>                           |



 

 

 



