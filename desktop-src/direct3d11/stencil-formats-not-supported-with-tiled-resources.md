---
title: Formats de stencil non pris en charge avec les ressources en mosaïque
description: Les formats qui contiennent le stencil ne sont pas pris en charge avec les ressources en mosaïque.
ms.assetid: 1B675245-F21F-47B5-B3B4-C8307DAC575B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce07b64e54808a2b4b730f6ed9c5321956f6bf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028489"
---
# <a name="stencil-formats-not-supported-with-tiled-resources"></a><span data-ttu-id="fc7ac-103">Formats de stencil non pris en charge avec les ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="fc7ac-103">Stencil formats not supported with tiled resources</span></span>

<span data-ttu-id="fc7ac-104">Les formats qui contiennent le stencil ne sont pas pris en charge avec les ressources en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="fc7ac-104">Formats that contain stencil aren't supported with tiled resources.</span></span>

<span data-ttu-id="fc7ac-105">Les formats qui contiennent le stencil incluent DXGI \_ format \_ D24 \_ UNORM \_ S8 \_ uint (et les formats associés dans la famille R24G8) et dxgi \_ format d32 \_ \_ float \_ S8X24 \_ uint (et les formats associés dans la famille R32G8X24).</span><span class="sxs-lookup"><span data-stu-id="fc7ac-105">Formats that contain stencil include DXGI\_FORMAT\_D24\_UNORM\_S8\_UINT (and related formats in the R24G8 family) and DXGI\_FORMAT\_D32\_FLOAT\_S8X24\_UINT (and related formats in the R32G8X24 family).</span></span>

<span data-ttu-id="fc7ac-106">Certaines implémentations stockent la profondeur et le stencil dans des allocations distinctes, tandis que d’autres les stockent ensemble.</span><span class="sxs-lookup"><span data-stu-id="fc7ac-106">Some implementations store depth and stencil in separate allocations while others store them together.</span></span> <span data-ttu-id="fc7ac-107">La gestion des vignettes pour les deux schémas devrait être différente et aucune API ne peut abstraire ou rationaliser les différences.</span><span class="sxs-lookup"><span data-stu-id="fc7ac-107">Tile management for the two schemes would have to be different, and no single API can abstract or rationalize the differences.</span></span> <span data-ttu-id="fc7ac-108">Nous vous recommandons d’utiliser du matériel pour prendre en charge des surfaces de stencil et de profondeur indépendantes, chacune étant présentée indépendamment.</span><span class="sxs-lookup"><span data-stu-id="fc7ac-108">We recommend for future hardware to support independent depth and stencil surfaces, each independently tiled.</span></span> <span data-ttu-id="fc7ac-109">la profondeur de 32 bits comporterait des vignettes 128 x 128 et le stencil de 8 bits aurait des vignettes 256x256.</span><span class="sxs-lookup"><span data-stu-id="fc7ac-109">32 bit depth would have 128x128 tiles, and 8 bit stencil would have 256x256 tiles.</span></span> <span data-ttu-id="fc7ac-110">Par conséquent, les applications doivent être en ligne avec un mauvais alignement de forme de vignette entre la profondeur et le gabarit.</span><span class="sxs-lookup"><span data-stu-id="fc7ac-110">Therefore, applications would have to live with tile shape misalignment between depth and stencil.</span></span> <span data-ttu-id="fc7ac-111">Mais le même problème existe déjà avec des formats de surface cible de rendu différents.</span><span class="sxs-lookup"><span data-stu-id="fc7ac-111">But the same problem exists with different render target surface formats already.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc7ac-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc7ac-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc7ac-113">Partage de ressources en mosaïque et partage d’appareils</span><span class="sxs-lookup"><span data-stu-id="fc7ac-113">Tiled resource cross process and device sharing</span></span>](tiled-resource-cross-process-and-device-sharing.md)
</dt> </dl>

 

 




