---
title: Suivi des risques ou ressources d’un pool de vignettes
description: Pour les ressources qui ne sont pas en mosaïque, Direct3D peut empêcher certaines conditions de danger pendant le rendu, mais comme le suivi des risques se trouve au niveau de la mosaïque pour les ressources en mosaïque, le suivi des conditions de danger lors du rendu des ressources en mosaïque peut être trop onéreux.
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75dcd11cb5e49f165105bd932854e36b37308cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379666"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a><span data-ttu-id="54728-103">Suivi des risques ou ressources d’un pool de vignettes</span><span class="sxs-lookup"><span data-stu-id="54728-103">Hazard tracking versus tile pool resources</span></span>

<span data-ttu-id="54728-104">Pour les ressources qui ne sont pas en mosaïque, Direct3D peut empêcher certaines conditions de danger pendant le rendu, mais comme le suivi des risques se trouve au niveau de la mosaïque pour les ressources en mosaïque, le suivi des conditions de danger lors du rendu des ressources en mosaïque peut être trop onéreux.</span><span class="sxs-lookup"><span data-stu-id="54728-104">For non-tiled resources, Direct3D can prevent certain hazard conditions during rendering, but because hazard tracking would be at a tile level for tiled resources, tracking hazard conditions during rendering of tiled resources might be too expensive.</span></span>

<span data-ttu-id="54728-105">Par exemple, pour les ressources non juxtaposées, le runtime n’autorise pas la liaison d’une sous-ressource donnée en tant qu’entrée (comme ShaderResourceView) et en tant que sortie (comme un RenderTargetView) en même temps.</span><span class="sxs-lookup"><span data-stu-id="54728-105">For example, for non-tiled resources, the runtime doesn't allow any given SubResource to be bound as an input (such as a ShaderResourceView) and as an output (such as a RenderTargetView) at the same time.</span></span> <span data-ttu-id="54728-106">Si un tel cas est rencontré, le runtime dissocie l’entrée.</span><span class="sxs-lookup"><span data-stu-id="54728-106">If such a case is encountered, the runtime unbinds the input.</span></span> <span data-ttu-id="54728-107">Cette surcharge de suivi dans le runtime est peu coûteuse et est effectuée au niveau de la sous-ressource.</span><span class="sxs-lookup"><span data-stu-id="54728-107">This tracking overhead in the runtime is cheap and is done at the SubResource level.</span></span> <span data-ttu-id="54728-108">L’un des avantages de cette surcharge de suivi est de réduire les risques d’applications par inadvertance en fonction de l’ordre d’exécution des nuanceurs matériels.</span><span class="sxs-lookup"><span data-stu-id="54728-108">One of the benefits of this tracking overhead is to minimize the chances of applications accidentally depending on hardware shader execution order.</span></span> <span data-ttu-id="54728-109">L’ordre d’exécution du nuanceur de matériel peut varier s’il n’est pas sur une unité de traitement graphique (GPU) donnée, alors que sur différents GPU.</span><span class="sxs-lookup"><span data-stu-id="54728-109">Hardware shader execution order can vary if not on a given graphics processing unit (GPU), then certainly across different GPUs.</span></span>

<span data-ttu-id="54728-110">Le suivi de la façon dont les ressources sont liées peut être trop coûteux pour les ressources en mosaïque, car le suivi se fait au niveau de la mosaïque.</span><span class="sxs-lookup"><span data-stu-id="54728-110">Tracking how resources are bound might be too expensive for tiled resources because tracking is at a tile level.</span></span> <span data-ttu-id="54728-111">De nouveaux problèmes se posent, tels que la validation éventuelle des tentatives de rendu sur un RenderTargetView avec une vignette mappée à plusieurs zones de la surface simultanément.</span><span class="sxs-lookup"><span data-stu-id="54728-111">New issues arise such as possibly validating away attempts to render to an RenderTargetView with one tile mapped to multiple areas in the surface simultaneously.</span></span> <span data-ttu-id="54728-112">S’il s’avère que ce suivi des risques par vignette est trop coûteux pour le runtime, l’idéal serait au moins une option dans la couche de débogage.</span><span class="sxs-lookup"><span data-stu-id="54728-112">If it turns out this per-tile hazard tracking is too expensive for the runtime, ideally this would at least be an option in the debug layer.</span></span>

<span data-ttu-id="54728-113">Une application doit informer le pilote d’affichage lorsqu’il a émis une opération d’écriture ou de lecture sur une ressource en mosaïque qui fait référence à la mémoire du pool de vignettes qui sera également référencée par des ressources en mosaïque distinctes dans les opérations de lecture ou d’écriture à venir, et que la première opération doit se terminer avant que les opérations suivantes puissent commencer.</span><span class="sxs-lookup"><span data-stu-id="54728-113">An application must inform the display driver when it has issued a write or read operation to a tiled resource that references tile pool memory that will also be referenced by separate tiled resources in upcoming read or write operations that it is expecting the first operation to complete before the following operations can begin.</span></span> <span data-ttu-id="54728-114">Pour plus d’informations sur cette condition, consultez la section Notes [**ID3D11DeviceContext2 :: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) .</span><span class="sxs-lookup"><span data-stu-id="54728-114">For more info about this condition, see [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) remarks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54728-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54728-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54728-116">Mappages dans un pool de vignettes</span><span class="sxs-lookup"><span data-stu-id="54728-116">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




