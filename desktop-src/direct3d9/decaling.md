---
description: Les applications Direct3D utilisent le décalqueing pour contrôler les pixels d’une image primitive particulière qui sont dessinés sur la surface cible de rendu. Les applications appliquent des dépassements aux images de primitives pour permettre l’affichage correct de polygones polygones.
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: Décalqueing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5606bdbc798d8b1e834aff53b04984f659af650
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108751"
---
# <a name="decaling-direct3d-9"></a><span data-ttu-id="2f533-104">Décalqueing (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2f533-104">Decaling (Direct3D 9)</span></span>

<span data-ttu-id="2f533-105">Les applications Direct3D utilisent le décalqueing pour contrôler les pixels d’une image primitive particulière qui sont dessinés sur la surface cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="2f533-105">Direct3D applications use decaling to control which pixels from a particular primitive image are drawn to the rendering target surface.</span></span> <span data-ttu-id="2f533-106">Les applications appliquent des dépassements aux images de primitives pour permettre l’affichage correct de polygones polygones.</span><span class="sxs-lookup"><span data-stu-id="2f533-106">Applications apply decals to the images of primitives to enable coplanar polygons to render correctly.</span></span>

<span data-ttu-id="2f533-107">Par exemple, lorsque vous appliquez des marques de pneu et des lignes jaunes à une chaussée, les marquages doivent apparaître directement en haut de la route.</span><span class="sxs-lookup"><span data-stu-id="2f533-107">For instance, when applying tire marks and yellow lines to a roadway, the markings should appear directly on top of the road.</span></span> <span data-ttu-id="2f533-108">Toutefois, les valeurs z des marquages et de la route sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="2f533-108">However, the z values of the markings and the road are the same.</span></span> <span data-ttu-id="2f533-109">Par conséquent, il se peut que la mémoire tampon de profondeur ne produise pas une séparation nette entre les deux.</span><span class="sxs-lookup"><span data-stu-id="2f533-109">Therefore, the depth buffer might not produce a clean separation between the two.</span></span> <span data-ttu-id="2f533-110">Certains pixels de la primitive arrière peuvent être rendus au-dessus de la primitive avant et vice versa.</span><span class="sxs-lookup"><span data-stu-id="2f533-110">Some pixels in the back primitive may be rendered on top of the front primitive and vice versa.</span></span> <span data-ttu-id="2f533-111">L’image résultante semble en scintillement du cadre au frame.</span><span class="sxs-lookup"><span data-stu-id="2f533-111">The resulting image appears to shimmer from frame to frame.</span></span> <span data-ttu-id="2f533-112">Cet effet est appelé *z-combat* ou *flimmering*.</span><span class="sxs-lookup"><span data-stu-id="2f533-112">This effect is called *z-fighting* or *flimmering*.</span></span>

<span data-ttu-id="2f533-113">Pour résoudre ce problème, utilisez un gabarit pour masquer la section de la primitive de retour où le décalcomanie s’affichera.</span><span class="sxs-lookup"><span data-stu-id="2f533-113">To solve this problem, use a stencil to mask the section of the back primitive where the decal will appear.</span></span> <span data-ttu-id="2f533-114">Désactivez la mise en mémoire tampon z et affichez l’image de la primitive avant dans la zone masquée de la surface de rendu-cible.</span><span class="sxs-lookup"><span data-stu-id="2f533-114">Turn off z-buffering and render the image of the front primitive into the masked-off area of the render-target surface.</span></span>

<span data-ttu-id="2f533-115">Bien que la combinaison de plusieurs textures puisse être utilisée pour résoudre ce problème, cela limite le nombre d’autres effets spéciaux que votre application peut produire.</span><span class="sxs-lookup"><span data-stu-id="2f533-115">Although multiple texture blending can be used to solve this problem, doing so limits the number of other special effects that your application can produce.</span></span> <span data-ttu-id="2f533-116">L’utilisation de la mémoire tampon de stencil pour appliquer des dépassements libère des étapes de fusion de texture pour d’autres effets.</span><span class="sxs-lookup"><span data-stu-id="2f533-116">Using the stencil buffer to apply decals frees up texture blending stages for other effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f533-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2f533-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f533-118">Techniques de tampon de stencil</span><span class="sxs-lookup"><span data-stu-id="2f533-118">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



