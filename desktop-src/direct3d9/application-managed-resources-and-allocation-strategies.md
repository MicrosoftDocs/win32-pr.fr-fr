---
description: Les ressources de mémoire tampon de vertex ou de mémoire tampon managée ne peuvent pas être déclarées dynamiques en spécifiant D3DUSAGE \_ Dynamic au moment de la création.
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Ressources de Application-Managed et stratégies d’allocation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f5ce23cac4bf46b8580a31d7c6d71fdc3de15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516169"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a><span data-ttu-id="552f2-103">Ressources de Application-Managed et stratégies d’allocation (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="552f2-103">Application-Managed Resources and Allocation Strategies (Direct3D 9)</span></span>

<span data-ttu-id="552f2-104">Les ressources de mémoire tampon de vertex ou de mémoire tampon managée ne peuvent pas être déclarées dynamiques en spécifiant D3DUSAGE \_ Dynamic au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="552f2-104">Managed vertex-buffer or index-buffer resources cannot be declared dynamic by specifying D3DUSAGE\_DYNAMIC at creation time.</span></span> <span data-ttu-id="552f2-105">Cela nécessite une copie supplémentaire pour chaque modification apportée au contenu de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="552f2-105">This would require an additional copy for every modification to the vertex buffer contents.</span></span> <span data-ttu-id="552f2-106">Les mémoires tampons de vertex dynamiques sont destinées au rendu de la géométrie dynamique et des données extraites à partir d’arborescences partitionnées d’espaces binaires ou d’autres structures de données de visibilité.</span><span class="sxs-lookup"><span data-stu-id="552f2-106">Dynamic vertex buffers are intended for rendering dynamic geometry and data pulled in from binary space partitioned trees or other visibility data structures.</span></span> <span data-ttu-id="552f2-107">Pour ce faire, vous devez préallouer les tampons du format souhaité.</span><span class="sxs-lookup"><span data-stu-id="552f2-107">This can be accomplished by pre-allocating buffers of the desired format.</span></span> <span data-ttu-id="552f2-108">Ces ressources sont ensuite représentées pour prendre en charge les besoins d’application par un gestionnaire de ressources au sein de l’application.</span><span class="sxs-lookup"><span data-stu-id="552f2-108">These resources are then parceled out to support application needs by a resource manager within the application.</span></span> <span data-ttu-id="552f2-109">Le nombre total de mémoires tampons de vertex dynamiques est faible, car une application n’utilise simultanément que quelques Strides de vertex différents et parce qu’une autre mémoire tampon de vertex est requise uniquement pour les Strides uniques.</span><span class="sxs-lookup"><span data-stu-id="552f2-109">The total number of dynamic vertex buffers is small because an application will use simultaneously only a few different vertex strides and because a different vertex buffer is required only for unique strides.</span></span> <span data-ttu-id="552f2-110">Lorsque vous gérez des ressources dynamiques de cette manière, assurez-vous que les demandes à fréquence élevée sur les ressources ne diminuent pas de manière significative les performances de l’application.</span><span class="sxs-lookup"><span data-stu-id="552f2-110">When managing dynamic resources in this way, ensure that high-frequency demands on the resources do not significantly decrease the application's performance.</span></span>

<span data-ttu-id="552f2-111">Lorsque vous utilisez des ressources gérées par Direct3D et des applications, allouez des ressources gérées par l’application dans la \_ mémoire par défaut D3DPOOL avant de créer des ressources gérées par Direct3D.</span><span class="sxs-lookup"><span data-stu-id="552f2-111">When using resources managed by both Direct3D and applications, allocate application-managed resources in D3DPOOL\_DEFAULT memory prior to creating Direct3D-managed resources.</span></span> <span data-ttu-id="552f2-112">Cela permet au gestionnaire de mémoire de conserver un nombre précis de mémoire disponible.</span><span class="sxs-lookup"><span data-stu-id="552f2-112">This enables the memory manager to maintain an accurate count of available memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="552f2-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="552f2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="552f2-114">Ressources Direct3D</span><span class="sxs-lookup"><span data-stu-id="552f2-114">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 



