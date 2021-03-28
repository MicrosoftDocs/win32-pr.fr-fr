---
title: Compression de mipmaps
description: En fonction du niveau de prise en charge des ressources en mosaïque, les des mipmaps avec certaines dimensions ne suivent pas les formes de mosaïque standard et sont considérées comme toutes regroupées les unes avec les autres d’une manière qui est opaque pour l’application.
ms.assetid: 3B416324-7656-495F-9BA9-8F5BE475ABC1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db4cd6f70129f46495673dfc82b5d261210ab21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028920"
---
# <a name="mipmap-packing"></a><span data-ttu-id="495e9-103">Compression de mipmaps</span><span class="sxs-lookup"><span data-stu-id="495e9-103">Mipmap packing</span></span>

<span data-ttu-id="495e9-104">En fonction du [niveau](tiled-resources-features-tiers.md) de prise en charge des ressources en mosaïque, les des mipmaps avec certaines dimensions ne suivent pas les formes de mosaïque standard et sont considérées comme toutes regroupées les unes avec les autres d’une manière qui est opaque pour l’application.</span><span class="sxs-lookup"><span data-stu-id="495e9-104">Depending on the [tier](tiled-resources-features-tiers.md) of tiled resources support, mipmaps with certain dimensions don't follow the standard tile shapes and are considered to all be packed together with one another in a manner that is opaque to the application.</span></span> <span data-ttu-id="495e9-105">Les niveaux supérieurs de la prise en charge ont des garanties plus larges sur les types de dimensions de surface qui tiennent dans les formes de mosaïque standard (et peuvent donc être mappées individuellement par les applications).</span><span class="sxs-lookup"><span data-stu-id="495e9-105">Higher tiers of support have broader guarantees about what types of surface dimensions fit in the standard tile shapes (and can therefore be individually mapped by applications).</span></span>

<span data-ttu-id="495e9-106">Ce qui peut varier entre les implémentations, c’est que, étant donné les dimensions, le format, le nombre de des mipmaps et les tranches de tableaux d’une ressource en mosaïque, un nombre M de MIPS (par tranche de groupe) peut être compressé dans un nombre N de vignettes.</span><span class="sxs-lookup"><span data-stu-id="495e9-106">What can vary between implementations is that—given a tiled resource's dimensions, format, number of mipmaps, and array slices—some number M of mips (per array slice) can be packed into some number N tiles.</span></span> <span data-ttu-id="495e9-107">L’API [**ID3D11Device2 :: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) permet au pilote de signaler à l’application les M et N suivants (parmi d’autres détails sur la surface que cette API signale comme standard et ne varient pas selon le fabricant du matériel).</span><span class="sxs-lookup"><span data-stu-id="495e9-107">The [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) API exists to allow the driver to report to the application what M and N are (among other details about the surface that this API reports that are standard and don't vary by hardware vendor).</span></span> <span data-ttu-id="495e9-108">L’ensemble de vignettes pour les mips compressés est toujours de 64 Ko et peut être mappé individuellement en emplacements disparates dans un pool de mosaïques.</span><span class="sxs-lookup"><span data-stu-id="495e9-108">The set of tiles for the packed mips are still 64KB and can be individually mapped into disparate locations in a tile pool.</span></span> <span data-ttu-id="495e9-109">Toutefois, la forme de pixel des vignettes et la façon dont les des mipmaps s’ajustent à l’ensemble des vignettes sont spécifiques à un fournisseur de matériel et trop complexes à exposer.</span><span class="sxs-lookup"><span data-stu-id="495e9-109">But the pixel shape of the tiles and how the mipmaps fit across the set of tiles is specific to a hardware vendor and too complex to expose.</span></span> <span data-ttu-id="495e9-110">Ainsi, les applications doivent mapper toutes les vignettes qui sont désignées comme compressées, ou aucune d’entre elles, à la fois.</span><span class="sxs-lookup"><span data-stu-id="495e9-110">So, applications are required to either map all of the tiles that are designated as packed, or none of them, at a time.</span></span> <span data-ttu-id="495e9-111">Dans le cas contraire, le comportement d’accès à la ressource en mosaïque n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="495e9-111">Otherwise, the behavior for accessing the tiled resource is undefined.</span></span>

<span data-ttu-id="495e9-112">Pour les surfaces groupées, l’ensemble des mips et le nombre de vignettes empaquetées qui stockent ces MIPS (M et N décrits précédemment) s’appliquent individuellement pour chaque tranche de tableau.</span><span class="sxs-lookup"><span data-stu-id="495e9-112">For arrayed surfaces, the set of packed mips and the number of packed tiles storing those mips (M and N described preceding) applies individually for each array slice.</span></span>

<span data-ttu-id="495e9-113">Les API dédiées pour la copie des vignettes ([**ID3D11DeviceContext2 :: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) et [**ID3D11DeviceContext2 :: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) ne peuvent pas accéder aux mips compressés.</span><span class="sxs-lookup"><span data-stu-id="495e9-113">Dedicated APIs for copying tiles ([**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) and [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) can't access packed mips.</span></span> <span data-ttu-id="495e9-114">Les applications qui souhaitent copier des données vers et depuis des mips compressés peuvent le faire à l’aide de toutes les API spécifiques à la ressource non en mosaïque pour la copie et le rendu des surfaces.</span><span class="sxs-lookup"><span data-stu-id="495e9-114">Applications that want to copy data to and from packed mips can do so using all the non-tiled resource specific APIs for copying and rendering to surfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="495e9-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="495e9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="495e9-116">Mode de mosaïque de la zone d’une ressource en mosaïque</span><span class="sxs-lookup"><span data-stu-id="495e9-116">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 




