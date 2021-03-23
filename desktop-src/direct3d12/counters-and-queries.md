---
title: Compteurs, requêtes et prédicats
description: La sortie de flux et les compteurs UAV fonctionnent dans Direct3D 12 dans une méthode similaire à Direct3D 11, bien que la mémoire pour les compteurs doive être allouée par l’application, le pilote ne le fait pas.
ms.assetid: 8BDDAFEF-57D4-4EF5-BB0C-6C96AF557A45
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314c01b05ac31e5d5f8348b775c8955ae382f5ed
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548594"
---
# <a name="counters-queries-and-predication"></a><span data-ttu-id="11e1f-103">Compteurs, requêtes et prédicats</span><span class="sxs-lookup"><span data-stu-id="11e1f-103">Counters, queries, and predication</span></span>

<span data-ttu-id="11e1f-104">Cette rubrique traite des compteurs de flux de sortie, des compteurs UAV, des requêtes et des prédicats.</span><span class="sxs-lookup"><span data-stu-id="11e1f-104">This topic covers stream-output counters, UAV counters, queries, and predication.</span></span>

<span data-ttu-id="11e1f-105">La sortie de flux et les compteurs UAV fonctionnent dans Direct3D 12 dans une méthode similaire à Direct3D 11, bien que la mémoire pour les compteurs doive être allouée par l’application, le pilote ne le fait pas.</span><span class="sxs-lookup"><span data-stu-id="11e1f-105">Stream output and UAV counters operate in Direct3D 12 in a similar method to Direct3D 11, although now memory for the counters must be allocated by the app, the driver does not do it.</span></span> <span data-ttu-id="11e1f-106">Les requêtes dans Direct3D 12 sont plus différentes de celles de Direct3D 11, avec l’ajout de clôtures et d’autres processus qui éliminent le besoin de certains types de requêtes.</span><span class="sxs-lookup"><span data-stu-id="11e1f-106">Queries in Direct3D 12 are more different from those in Direct3D 11, with the addition of fences and other processes that remove the need for some query types.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="11e1f-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="11e1f-107">In this section</span></span>



| <span data-ttu-id="11e1f-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="11e1f-108">Topic</span></span>                                                           | <span data-ttu-id="11e1f-109">Description</span><span class="sxs-lookup"><span data-stu-id="11e1f-109">Description</span></span>                                                                                                                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11e1f-110">Compteurs de sortie de flux</span><span class="sxs-lookup"><span data-stu-id="11e1f-110">Stream Output Counters</span></span>](stream-output-counters.md)<br/> | <span data-ttu-id="11e1f-111">La sortie de flux est la capacité du GPU à écrire des vertex dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="11e1f-111">Stream output is the ability of the GPU to write vertices to a buffer.</span></span> <span data-ttu-id="11e1f-112">Les compteurs de sortie de flux surveillent la progression.</span><span class="sxs-lookup"><span data-stu-id="11e1f-112">The stream output counters monitor progress.</span></span><br/>                                                               |
| [<span data-ttu-id="11e1f-113">Compteurs UAV</span><span class="sxs-lookup"><span data-stu-id="11e1f-113">UAV Counters</span></span>](uav-counters.md)<br/>                     | <span data-ttu-id="11e1f-114">Les compteurs UAV peuvent être utilisés pour associer un compteur atomique 32 bits à un mode d’accès non ordonné (UAV).</span><span class="sxs-lookup"><span data-stu-id="11e1f-114">UAV counters can be used to associate a 32-bit atomic counter with an unordered-access-view (UAV).</span></span><br/>                                                                                |
| [<span data-ttu-id="11e1f-115">Requêtes</span><span class="sxs-lookup"><span data-stu-id="11e1f-115">Queries</span></span>](queries.md)<br/>                               | <span data-ttu-id="11e1f-116">Dans Direct3D 12, les requêtes sont regroupées en tableaux de requêtes appelé segment de requête.</span><span class="sxs-lookup"><span data-stu-id="11e1f-116">In Direct3D 12, queries are grouped into arrays of queries called a query heap.</span></span> <span data-ttu-id="11e1f-117">Un segment de mémoire de requête a un type qui définit les types de requêtes valides qui peuvent être utilisés avec ce tas.</span><span class="sxs-lookup"><span data-stu-id="11e1f-117">A query heap has a type which defines the valid types of queries that can be used with that heap.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="11e1f-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="11e1f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11e1f-119">Mesure des performances</span><span class="sxs-lookup"><span data-stu-id="11e1f-119">Performance Measurement</span></span>](performance-measurement.md)
</dt> </dl>

 

 





