---
title: Mosaïque de mémoires tampons
description: Une ressource de mémoire tampon est divisée en mosaïques de 64 Ko, avec un espace vide dans la dernière vignette si la taille n’est pas un multiple de 64 Ko.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fafa009e554499822c90c8fb6c0c8f34e47f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842357"
---
# <a name="buffer-tiling"></a><span data-ttu-id="f157d-103">Mosaïque de mémoires tampons</span><span class="sxs-lookup"><span data-stu-id="f157d-103">Buffer tiling</span></span>

<span data-ttu-id="f157d-104">Une ressource de [mémoire tampon](overviews-direct3d-11-resources-buffers.md) est divisée en mosaïques de 64 Ko, avec un espace vide dans la dernière vignette si la taille n’est pas un multiple de 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="f157d-104">A [Buffer](overviews-direct3d-11-resources-buffers.md) resource is divided into 64KB tiles, with some empty space in the last tile if the size is not a multiple of 64KB.</span></span>

<span data-ttu-id="f157d-105">Les mémoires tampons structurées ne doivent pas avoir de contrainte sur le STRIDE à présenter en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="f157d-105">Structured buffers must have no constraint on the stride to be tiled.</span></span> <span data-ttu-id="f157d-106">Toutefois, les optimisations de performances possibles dans le matériel pour l’utilisation de [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) peuvent être sacrifiées en les mettant en mosaïque en premier lieu.</span><span class="sxs-lookup"><span data-stu-id="f157d-106">But possible performance optimizations in hardware for using [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) can be sacrificed by making them tiled in the first place.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f157d-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f157d-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f157d-108">Mode de mosaïque de la zone d’une ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="f157d-108">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 