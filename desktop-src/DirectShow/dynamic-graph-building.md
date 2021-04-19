---
description: Génération de graphiques dynamiques
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: Génération de graphiques dynamiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710bf5f648fc91e8db6bf62d81b41327f874ddf7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544549"
---
# <a name="dynamic-graph-building"></a><span data-ttu-id="d407e-103">Génération de graphiques dynamiques</span><span class="sxs-lookup"><span data-stu-id="d407e-103">Dynamic Graph Building</span></span>

<span data-ttu-id="d407e-104">Si vous avez besoin de modifier un graphique de filtre existant, vous pouvez arrêter le graphique, apporter les modifications et redémarrer le graphique.</span><span class="sxs-lookup"><span data-stu-id="d407e-104">If you need to modify an existing filter graph, you can stop the graph, make the changes, and restart the graph.</span></span> <span data-ttu-id="d407e-105">Il s’agit généralement de la meilleure approche.</span><span class="sxs-lookup"><span data-stu-id="d407e-105">This is usually the best approach.</span></span> <span data-ttu-id="d407e-106">Toutefois, dans certaines circonstances, vous souhaiterez peut-être modifier un graphique pendant qu’il est toujours en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d407e-106">However, under some circumstances, you might want to alter a graph while it is still running.</span></span> <span data-ttu-id="d407e-107">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="d407e-107">For example:</span></span>

-   <span data-ttu-id="d407e-108">L’application insère un filtre d’effets vidéo pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="d407e-108">The application inserts a video effects filter during playback.</span></span>
-   <span data-ttu-id="d407e-109">Un filtre source change de type de média pendant, ce qui peut nécessiter un nouveau filtre de décompression.</span><span class="sxs-lookup"><span data-stu-id="d407e-109">A source filter switches media types midstream, possibly requiring a new decompression filter.</span></span>
-   <span data-ttu-id="d407e-110">L’application ajoute un nouveau flux vidéo au graphique.</span><span class="sxs-lookup"><span data-stu-id="d407e-110">The application adds a new video stream to the graph.</span></span>

<span data-ttu-id="d407e-111">Il s’agit de tous les exemples de *création de graphique dynamique*, terme qui couvre tout type de modification apportée à un graphique de filtre pendant que le graphique continue à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="d407e-111">These are all examples of *dynamic graph building*, a term that covers any kind of change to a filter graph while the graph continues to run.</span></span> <span data-ttu-id="d407e-112">La génération de graphiques dynamiques peut être lancée par une application ou par un filtre dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="d407e-112">Dynamic graph building can be initiated by an application or by a filter in the graph.</span></span> <span data-ttu-id="d407e-113">Trois scénarios distincts sont possibles :</span><span class="sxs-lookup"><span data-stu-id="d407e-113">Three distinct scenarios are possible:</span></span>

-   <span data-ttu-id="d407e-114">[Modifications de format dynamique](dynamic-format-changes.md): un filtre peut changer les formats pendant, sans qu’il soit nécessaire de supprimer ou de remplacer des filtres.</span><span class="sxs-lookup"><span data-stu-id="d407e-114">[Dynamic Format Changes](dynamic-format-changes.md): A filter can change formats midstream, without the need to remove or replace any filters.</span></span>
-   <span data-ttu-id="d407e-115">[Reconnexion dynamique](dynamic-reconnection.md): modification du graphique en ajoutant ou en supprimant des filtres.</span><span class="sxs-lookup"><span data-stu-id="d407e-115">[Dynamic Reconnection](dynamic-reconnection.md): Changing the graph by adding or removing filters.</span></span>
-   <span data-ttu-id="d407e-116">[Chaînes de filtre](filter-chains.md): ajout, suppression et contrôle des chaînes de filtres.</span><span class="sxs-lookup"><span data-stu-id="d407e-116">[Filter Chains](filter-chains.md): Adding, removing, and controlling chains of filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d407e-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d407e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d407e-118">À propos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="d407e-118">About DirectShow</span></span>](about-directshow.md)
</dt> </dl>

 

 



