---
description: La fusion alpha de la mémoire tampon de frame est un peu différente du vertex alpha, du matériau alpha et de la texture alpha.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Mémoire tampon de trame alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb310e2c66f43282e65425fd0d6c6a24961accaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108739"
---
# <a name="frame-buffer-alpha-direct3d-9"></a><span data-ttu-id="631d8-103">Mémoire tampon de trame alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="631d8-103">Frame Buffer Alpha (Direct3D 9)</span></span>

<span data-ttu-id="631d8-104">La fusion alpha de la mémoire tampon de frame est un peu différente du vertex alpha, du matériau alpha et de la texture alpha.</span><span class="sxs-lookup"><span data-stu-id="631d8-104">Frame buffer alpha-blending is a bit different than vertex alpha, material alpha, and texture alpha.</span></span> <span data-ttu-id="631d8-105">Les valeurs de transparence de jeu alpha de vertex, de matériau et de texture, qui sont utilisées uniquement pour la primitive actuelle, et qui n’ont pas d’effet sur d’autres Primitives.</span><span class="sxs-lookup"><span data-stu-id="631d8-105">Vertex, material, and texture alpha set transparency values that are used only for the current primitive, and by themselves have no effect on other primitives.</span></span> <span data-ttu-id="631d8-106">La fonction de fusion alpha de la mémoire tampon de trame contrôle la manière dont la primitive actuelle est combinée avec les pixels existants dans la mémoire tampon de trame pour produire une couleur de pixel finale.</span><span class="sxs-lookup"><span data-stu-id="631d8-106">Frame buffer alpha-blending controls how the current primitive is combined with existing pixels in the frame buffer to yield a final pixel color.</span></span>

<span data-ttu-id="631d8-107">Lors de l’exécution de la fusion alpha, deux couleurs sont combinées : une couleur source et une couleur de destination.</span><span class="sxs-lookup"><span data-stu-id="631d8-107">When performing alpha blending, two colors are being combined: a source color and a destination color.</span></span> <span data-ttu-id="631d8-108">La couleur source provient de l’objet transparent, la couleur de destination est la couleur qui figure déjà à l’emplacement du pixel.</span><span class="sxs-lookup"><span data-stu-id="631d8-108">The source color is from the transparent object, the destination color is the color already at the pixel location.</span></span> <span data-ttu-id="631d8-109">La couleur de destination est le résultat du rendu d’un autre objet qui se trouve derrière l’objet transparent, autrement dit, l’objet qui sera visible via l’objet transparent.</span><span class="sxs-lookup"><span data-stu-id="631d8-109">The destination color is the result of rendering some other object that is behind the transparent object, that is, the object that will be visible through the transparent object.</span></span> <span data-ttu-id="631d8-110">La fusion alpha utilise une formule pour contrôler le rapport entre les objets source et de destination.</span><span class="sxs-lookup"><span data-stu-id="631d8-110">Alpha blending uses a formula to control the ratio between the source and destination objects.</span></span>


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



<span data-ttu-id="631d8-111">ObjectColor est la contribution de la primitive rendue à l’emplacement de pixel actuel.</span><span class="sxs-lookup"><span data-stu-id="631d8-111">ObjectColor is the contribution from the primitive being rendered at the current pixel location.</span></span> <span data-ttu-id="631d8-112">PixelColor est la contribution de la mémoire tampon de trame à l’emplacement actuel du pixel.</span><span class="sxs-lookup"><span data-stu-id="631d8-112">PixelColor is the contribution from the frame buffer at the current pixel location.</span></span>

<span data-ttu-id="631d8-113">L’ensemble des facteurs alpha Blend qui peuvent être utilisés sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="631d8-113">The set of alpha blend factors that can be used are listed below.</span></span>



| <span data-ttu-id="631d8-114">Facteur de mode de fusion</span><span class="sxs-lookup"><span data-stu-id="631d8-114">Blend mode factor</span></span>         | <span data-ttu-id="631d8-115">Description</span><span class="sxs-lookup"><span data-stu-id="631d8-115">Description</span></span>                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="631d8-116">D3DBLEND \_ zéro</span><span class="sxs-lookup"><span data-stu-id="631d8-116">D3DBLEND\_ZERO</span></span>            | <span data-ttu-id="631d8-117">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="631d8-117">(0, 0, 0, 0)</span></span>                                                                                                                                                                             |
| <span data-ttu-id="631d8-118">D3DBLEND \_ un</span><span class="sxs-lookup"><span data-stu-id="631d8-118">D3DBLEND\_ONE</span></span>             | <span data-ttu-id="631d8-119">(1, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="631d8-119">(1, 1, 1, 1)</span></span>                                                                                                                                                                             |
| <span data-ttu-id="631d8-120">D3DBLEND \_ SRCCOLOR</span><span class="sxs-lookup"><span data-stu-id="631d8-120">D3DBLEND\_SRCCOLOR</span></span>        | <span data-ttu-id="631d8-121">(RS, GS, BS, As)</span><span class="sxs-lookup"><span data-stu-id="631d8-121">(Rs, Gs, Bs, As)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="631d8-122">D3DBLEND \_ INVSRCCOLOR</span><span class="sxs-lookup"><span data-stu-id="631d8-122">D3DBLEND\_INVSRCCOLOR</span></span>     | <span data-ttu-id="631d8-123">(1-RS, 1-GS, 1-BS, 1-As)</span><span class="sxs-lookup"><span data-stu-id="631d8-123">(1-Rs, 1-Gs, 1-Bs, 1-As)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="631d8-124">D3DBLEND \_ SRCALPHA</span><span class="sxs-lookup"><span data-stu-id="631d8-124">D3DBLEND\_SRCALPHA</span></span>        | <span data-ttu-id="631d8-125">(As, As, As, As)</span><span class="sxs-lookup"><span data-stu-id="631d8-125">(As, As, As, As)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="631d8-126">D3DBLEND \_ INVSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="631d8-126">D3DBLEND\_INVSRCALPHA</span></span>     | <span data-ttu-id="631d8-127">(1-As, 1-As, 1-As, 1-As)</span><span class="sxs-lookup"><span data-stu-id="631d8-127">(1-As, 1-As, 1-As, 1-As)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="631d8-128">D3DBLEND \_ DESTALPHA</span><span class="sxs-lookup"><span data-stu-id="631d8-128">D3DBLEND\_DESTALPHA</span></span>       | <span data-ttu-id="631d8-129">(AD, ad, ad, AD)</span><span class="sxs-lookup"><span data-stu-id="631d8-129">(Ad, Ad, Ad, Ad)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="631d8-130">D3DBLEND \_ INVDESTALPHA</span><span class="sxs-lookup"><span data-stu-id="631d8-130">D3DBLEND\_INVDESTALPHA</span></span>    | <span data-ttu-id="631d8-131">(1-AD, 1-AD, 1-AD, 1-AD)</span><span class="sxs-lookup"><span data-stu-id="631d8-131">(1-Ad, 1-Ad, 1-Ad, 1-Ad)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="631d8-132">D3DBLEND \_ DESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="631d8-132">D3DBLEND\_DESTCOLOR</span></span>       | <span data-ttu-id="631d8-133">(Rd, GD, BD, AD)</span><span class="sxs-lookup"><span data-stu-id="631d8-133">(Rd, Gd, Bd, Ad)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="631d8-134">D3DBLEND \_ INVDESTCOLOR</span><span class="sxs-lookup"><span data-stu-id="631d8-134">D3DBLEND\_INVDESTCOLOR</span></span>    | <span data-ttu-id="631d8-135">(1-Rd, 1-gd, 1-BD, 1-AD)</span><span class="sxs-lookup"><span data-stu-id="631d8-135">(1-Rd, 1-Gd, 1-Bd, 1-Ad)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="631d8-136">D3DBLEND \_ SRCALPHASAT</span><span class="sxs-lookup"><span data-stu-id="631d8-136">D3DBLEND\_SRCALPHASAT</span></span>     | <span data-ttu-id="631d8-137">(f, f, f, 1); f = min (As, 1-AD)</span><span class="sxs-lookup"><span data-stu-id="631d8-137">(f, f, f, 1); f = min(As, 1-Ad)</span></span>                                                                                                                                                          |
| <span data-ttu-id="631d8-138">D3DBLEND \_ BOTHSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="631d8-138">D3DBLEND\_BOTHSRCALPHA</span></span>    | <span data-ttu-id="631d8-139">Obsolète pour DirectX 6 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="631d8-139">Obsolete for DirectX 6 and later.</span></span> <span data-ttu-id="631d8-140">Vous pouvez obtenir le même effet en définissant les facteurs de fusion source et destination sur D3DBLEND \_ SRCALPHA et D3DBLEND \_ INVSRCALPHA dans des appels distincts.</span><span class="sxs-lookup"><span data-stu-id="631d8-140">You can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span> |
| <span data-ttu-id="631d8-141">D3DBLEND \_ BOTHINVSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="631d8-141">D3DBLEND\_BOTHINVSRCALPHA</span></span> | <span data-ttu-id="631d8-142">Obsolète pour DirectX 6.</span><span class="sxs-lookup"><span data-stu-id="631d8-142">Obsolete for DirectX 6.</span></span> <span data-ttu-id="631d8-143">Vous pouvez obtenir le même effet en définissant les facteurs de fusion source et destination sur D3DBLEND \_ INVSRCALPHA et D3DBLEND \_ SRCALPHA dans des appels distincts.</span><span class="sxs-lookup"><span data-stu-id="631d8-143">You can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_INVSRCALPHA and D3DBLEND\_SRCALPHA in separate calls.</span></span>           |
| <span data-ttu-id="631d8-144">D3DBLEND \_ BLENDFACTOR</span><span class="sxs-lookup"><span data-stu-id="631d8-144">D3DBLEND\_BLENDFACTOR</span></span>     | <span data-ttu-id="631d8-145">Utilisez Color. r, Color. g, Color. b et Color. a obtenu à partir du \_ paramètre D3DRS BLENDFACTOR.</span><span class="sxs-lookup"><span data-stu-id="631d8-145">Use color.r, color.g, color.b, and color.a obtained from the D3DRS\_BLENDFACTOR setting.</span></span>                                                                                                 |
| <span data-ttu-id="631d8-146">D3DBLEND \_ INVBLENDFACTOR</span><span class="sxs-lookup"><span data-stu-id="631d8-146">D3DBLEND\_INVBLENDFACTOR</span></span>  | <span data-ttu-id="631d8-147">Utilisez 1-Color. r, 1-Color. g, 1-Color. b et 1-Color. a obtenu à partir du \_ paramètre D3DRS BLENDFACTOR.</span><span class="sxs-lookup"><span data-stu-id="631d8-147">Use 1-color.r, 1-color.g, 1-color.b, and 1-color.a obtained from the D3DRS\_BLENDFACTOR setting.</span></span>                                                                                         |



 

<span data-ttu-id="631d8-148">Direct3D utilise l' \_ État de rendu D3DRS ALPHABLENDENABLE pour activer la fusion de la transparence alpha.</span><span class="sxs-lookup"><span data-stu-id="631d8-148">Direct3D uses the D3DRS\_ALPHABLENDENABLE render state to enable alpha transparency blending.</span></span> <span data-ttu-id="631d8-149">Le type de fusion alpha effectué dépend des \_ États de rendu D3DRS SRCBLEND et D3DRS \_ DESTBLEND.</span><span class="sxs-lookup"><span data-stu-id="631d8-149">The type of alpha blending that is done depends on the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span> <span data-ttu-id="631d8-150">Les États de fusion de source et de destination sont utilisés par paires.</span><span class="sxs-lookup"><span data-stu-id="631d8-150">Source and destination blend states are used in pairs.</span></span> <span data-ttu-id="631d8-151">Le fragment de code suivant définit l’état de fusion source sur D3DBLEND \_ SRCCOLOR et l’état de fusion de destination sur D3DBLEND \_ INVSRCCOLOR.</span><span class="sxs-lookup"><span data-stu-id="631d8-151">The following code fragment sets the source blend state to D3DBLEND\_SRCCOLOR and the destination blend state to D3DBLEND\_INVSRCCOLOR.</span></span>


```
// This code fragment assumes that lpD3DDevice is a 
//   valid pointer to a device.

// Enable alpha blending.
lpD3DDevice->SetRenderState(D3DRS_ALPHABLENDENABLE, 
                            TRUE);

// Set the source blend state.
lpD3DDevice->SetRenderState(D3DRS_SRCBLEND, 
                            D3DBLEND_SRCCOLOR);

// Set the destination blend state.
lpD3DDevice->SetRenderState(D3DRS_DESTBLEND, 
                            D3DBLEND_INVSRCCOLOR);
```



<span data-ttu-id="631d8-152">Ce code effectue un mélange linéaire entre la couleur source (la couleur de la primitive rendue à l’emplacement actuel) et la couleur de destination (la couleur à l’emplacement actuel dans la mémoire tampon de trame).</span><span class="sxs-lookup"><span data-stu-id="631d8-152">This code performs a linear blend between the source color (the color of the primitive being rendered at the current location) and the destination color (the color at the current location in the frame buffer).</span></span> <span data-ttu-id="631d8-153">L’apparence qui en résulte est semblable au verre teinté, car une partie de la couleur de l’objet de destination semble être transmise via l’objet source. le reste de celui-ci semble être absorbé.</span><span class="sxs-lookup"><span data-stu-id="631d8-153">The resulting appearance is similar to tinted glass in that some of the color of the destination object seems to be transmitted through the source object; the rest of it appears to be absorbed.</span></span>

<span data-ttu-id="631d8-154">La plupart de ces facteurs de mélange nécessitent des valeurs alpha dans la texture pour fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="631d8-154">Many of these blend factors require alpha values in the texture to operate correctly.</span></span> <span data-ttu-id="631d8-155">Ainsi, lorsque vous utilisez un vertex ou un matériau alpha, l’application est limitée quant aux modes qui produiront des résultats intéressants.</span><span class="sxs-lookup"><span data-stu-id="631d8-155">Thus, when using vertex or material alpha, the application is restricted as to which modes will produce interesting results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="631d8-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="631d8-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="631d8-157">Fusion alpha</span><span class="sxs-lookup"><span data-stu-id="631d8-157">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



