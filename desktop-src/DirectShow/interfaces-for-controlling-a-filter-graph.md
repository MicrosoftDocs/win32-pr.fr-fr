---
description: Interfaces pour le contrôle d’un graphique de filtre
ms.assetid: f7de0165-e356-45d5-baed-d127caeebaf6
title: Interfaces pour le contrôle d’un graphique de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e88dc4ba2143bbbf33a58763a5ff9005254236
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747108"
---
# <a name="interfaces-for-controlling-a-filter-graph"></a><span data-ttu-id="c530c-103">Interfaces pour le contrôle d’un graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="c530c-103">Interfaces for Controlling a Filter Graph</span></span>

<span data-ttu-id="c530c-104">Ces interfaces fournissent des méthodes pour le contrôle d’un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="c530c-104">These interfaces provide methods for controlling a filter graph.</span></span>



| <span data-ttu-id="c530c-105">Interface</span><span class="sxs-lookup"><span data-stu-id="c530c-105">Interface</span></span>                                  | <span data-ttu-id="c530c-106">Description</span><span class="sxs-lookup"><span data-stu-id="c530c-106">Description</span></span>                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c530c-107">**IAMClockAdjust**</span><span class="sxs-lookup"><span data-stu-id="c530c-107">**IAMClockAdjust**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)   | <span data-ttu-id="c530c-108">Ajustez l’horloge du graphique.</span><span class="sxs-lookup"><span data-stu-id="c530c-108">Adjust the graph clock.</span></span>                                                                                   |
| [<span data-ttu-id="c530c-109">**IAMGraphStreams**</span><span class="sxs-lookup"><span data-stu-id="c530c-109">**IAMGraphStreams**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams) | <span data-ttu-id="c530c-110">Synchroniser des flux en direct dans un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="c530c-110">Synchronize live streams in a filter graph.</span></span>                                                               |
| [<span data-ttu-id="c530c-111">**IFilterChain**</span><span class="sxs-lookup"><span data-stu-id="c530c-111">**IFilterChain**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)       | <span data-ttu-id="c530c-112">Chaînes de contrôle des filtres.</span><span class="sxs-lookup"><span data-stu-id="c530c-112">Control chains of filters.</span></span>                                                                                |
| [<span data-ttu-id="c530c-113">**Appel**</span><span class="sxs-lookup"><span data-stu-id="c530c-113">**IMediaControl**</span></span>](/windows/desktop/api/Control/nn-control-imediacontrol)     | <span data-ttu-id="c530c-114">Exécutez, suspendez et arrêtez le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="c530c-114">Run, pause, and stop the filter graph.</span></span> <span data-ttu-id="c530c-115">(Fournit également des méthodes compatibles Automation pour la génération de graphiques.)</span><span class="sxs-lookup"><span data-stu-id="c530c-115">(Also provides Automation-compatible methods for building graphs.)</span></span> |
| [<span data-ttu-id="c530c-116">**IMediaEventEx**</span><span class="sxs-lookup"><span data-stu-id="c530c-116">**IMediaEventEx**</span></span>](/windows/desktop/api/Control/nn-control-imediaeventex)     | <span data-ttu-id="c530c-117">Répondre aux événements dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="c530c-117">Respond to events in the graph.</span></span>                                                                           |
| [<span data-ttu-id="c530c-118">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="c530c-118">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)     | <span data-ttu-id="c530c-119">Recherchez dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="c530c-119">Seek within a file.</span></span>                                                                                       |
| [<span data-ttu-id="c530c-120">**IQueueCommand**</span><span class="sxs-lookup"><span data-stu-id="c530c-120">**IQueueCommand**</span></span>](/windows/desktop/api/Control/nn-control-iqueuecommand)     | <span data-ttu-id="c530c-121">Met en file d’attente les commandes à exécuter ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="c530c-121">Queue commands to run at a later time.</span></span>                                                                    |
| [<span data-ttu-id="c530c-122">**IVideoFrameStep**</span><span class="sxs-lookup"><span data-stu-id="c530c-122">**IVideoFrameStep**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) | <span data-ttu-id="c530c-123">Effectuer un pas à pas détaillé dans un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="c530c-123">Frame-step through a video stream.</span></span>                                                                        |



 

 

 



