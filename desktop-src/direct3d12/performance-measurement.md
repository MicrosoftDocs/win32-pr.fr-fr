---
title: Compteurs, requêtes et mesure de performance
description: Les sections suivantes décrivent les fonctionnalités à utiliser dans les tests et l’amélioration des performances, tels que les requêtes, les compteurs, le minutage et la prédicat.
ms.assetid: C7AEF1A0-36FB-4026-9CCF-ED0206961A58
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf316978f3dd0928692f378dd8d72b8453ad0aae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104388"
---
# <a name="counters-queries-and-performance-measurement"></a><span data-ttu-id="edf12-103">Compteurs, requêtes et mesure de performance</span><span class="sxs-lookup"><span data-stu-id="edf12-103">Counters, Queries and Performance Measurement</span></span>

<span data-ttu-id="edf12-104">Les sections suivantes décrivent les fonctionnalités à utiliser dans les tests et l’amélioration des performances, tels que les requêtes, les compteurs, le minutage et la prédicat.</span><span class="sxs-lookup"><span data-stu-id="edf12-104">The following sections describe features for use in performance testing and improvement, such as queries, counters, timing, and predication.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="edf12-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="edf12-105">In this section</span></span>



| <span data-ttu-id="edf12-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="edf12-106">Topic</span></span>                                                                                                 | <span data-ttu-id="edf12-107">Description</span><span class="sxs-lookup"><span data-stu-id="edf12-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="edf12-108">Compteurs de flux de sortie, compteurs de UAV, requêtes et prédicats</span><span class="sxs-lookup"><span data-stu-id="edf12-108">Stream-Output Counters, UAV Counters, Queries, and Predication</span></span>](counters-and-queries.md)<br/> | <span data-ttu-id="edf12-109">La sortie de flux et les compteurs UAV fonctionnent dans Direct3D 12 dans une méthode similaire à Direct3D 11, bien que la mémoire pour les compteurs doive être allouée par l’application, le pilote ne le fait pas.</span><span class="sxs-lookup"><span data-stu-id="edf12-109">Stream output and UAV counters operate in Direct3D 12 in a similar method to Direct3D 11, although now memory for the counters must be allocated by the app, the driver does not do it.</span></span> <span data-ttu-id="edf12-110">Les requêtes dans Direct3D 12 sont plus différentes de celles de Direct3D 11, avec l’ajout de clôtures et d’autres processus qui éliminent le besoin de certains types de requêtes.</span><span class="sxs-lookup"><span data-stu-id="edf12-110">Queries in Direct3D 12 are more different from those in Direct3D 11, with the addition of fences and other processes that remove the need for some query types.</span></span><br/> |
| [<span data-ttu-id="edf12-111">Minutage</span><span class="sxs-lookup"><span data-stu-id="edf12-111">Timing</span></span>](timing.md)<br/>                                                                       | <span data-ttu-id="edf12-112">Cette section traite de l’interrogation des horodateurs et de l’étalonnage des compteurs GPU et horodateur de l’UC.</span><span class="sxs-lookup"><span data-stu-id="edf12-112">This section covers querying timestamps, and calibrating the GPU and CPU timestamp counters.</span></span><br/>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="edf12-113">Prédication</span><span class="sxs-lookup"><span data-stu-id="edf12-113">Predication</span></span>](predication.md)<br/>                                                             | <span data-ttu-id="edf12-114">Un prédicat est une fonctionnalité qui permet au GPU plutôt qu’au processeur de déterminer de ne pas dessiner, copier ou distribuer un objet.</span><span class="sxs-lookup"><span data-stu-id="edf12-114">Predication is a feature that enables the GPU rather than the CPU to determine to not draw, copy or dispatch an object.</span></span><br/>                                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="edf12-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="edf12-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edf12-116">Guide de programmation Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="edf12-116">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

 





