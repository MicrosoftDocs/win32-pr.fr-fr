---
description: Le moteur d’éclairage combine la couleur matérielle, la couleur du vertex et les informations d’éclairage pour générer une couleur par vertex.
ms.assetid: 1e7c31cb-dc63-4f4a-9ddc-d1d1d0b69085
title: Fusion de texture alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad394b70b96e17b2ce858f871fb869afde0d122
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513149"
---
# <a name="alpha-texture-blending-direct3d-9"></a><span data-ttu-id="d54d1-103">Fusion de texture alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d54d1-103">Alpha Texture Blending (Direct3D 9)</span></span>

<span data-ttu-id="d54d1-104">Le moteur d’éclairage combine la couleur matérielle, la couleur du vertex et les informations d’éclairage pour générer une couleur par vertex.</span><span class="sxs-lookup"><span data-stu-id="d54d1-104">The lighting engine combines material color, vertex color, and lighting information to generate a per-vertex color.</span></span> <span data-ttu-id="d54d1-105">Une fois interpolées, cela génère une couleur par pixel qui est écrite dans la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="d54d1-105">Once interpolated, this generates a per-pixel color that is written to the frame buffer.</span></span> <span data-ttu-id="d54d1-106">Si une application active la fusion de texture, la couleur de pixel devient une combinaison du pixel actuel dans la mémoire tampon de frame et une couleur de texture.</span><span class="sxs-lookup"><span data-stu-id="d54d1-106">If an application enables texture blending, the pixel color will become a combination of the current pixel in the frame buffer and a texture color.</span></span>

<span data-ttu-id="d54d1-107">Cette formule détermine la couleur finale du pixel fusionné :</span><span class="sxs-lookup"><span data-stu-id="d54d1-107">This formula determines the final blended pixel color:</span></span>


```
Color = TexelColor x SourceBlend + CurrentPixelColor x DestBlend
```



<span data-ttu-id="d54d1-108">Où :</span><span class="sxs-lookup"><span data-stu-id="d54d1-108">Where:</span></span>

-   <span data-ttu-id="d54d1-109">La couleur est la couleur de pixel de sortie.</span><span class="sxs-lookup"><span data-stu-id="d54d1-109">Color is the output pixel color.</span></span>
-   <span data-ttu-id="d54d1-110">TexelColor est la couleur d’entrée après le filtrage de texture.</span><span class="sxs-lookup"><span data-stu-id="d54d1-110">TexelColor is the input color after texture filtering.</span></span>
-   <span data-ttu-id="d54d1-111">SourceBlend est le pourcentage de la couleur de pixel finale qui est constitué de la couleur Texel source.</span><span class="sxs-lookup"><span data-stu-id="d54d1-111">SourceBlend is the percentage of the final pixel color that is made up of the source texel color.</span></span>
-   <span data-ttu-id="d54d1-112">CurrentPixelColor est la couleur du pixel actuel.</span><span class="sxs-lookup"><span data-stu-id="d54d1-112">CurrentPixelColor is the color of the current pixel.</span></span>
-   <span data-ttu-id="d54d1-113">DestBlend est le pourcentage de la couleur de pixel finale qui est constitué de la couleur de pixel actuelle.</span><span class="sxs-lookup"><span data-stu-id="d54d1-113">DestBlend is the percentage of the final pixel color that is made up of the current pixel color.</span></span>

<span data-ttu-id="d54d1-114">L’équation de fusion finale est définie en appelant [**IDirect3DDevice9 :: SetRenderState**](/windows/desktop/api) et en spécifiant l’état de rendu Blend (D3DRS \_ BLENDXXX) avec un facteur de fusion correspondant ([**D3DBLEND**](./d3dblend.md)).</span><span class="sxs-lookup"><span data-stu-id="d54d1-114">The final blending equation is set by calling [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) and specifying the blend render state (D3DRS\_BLENDXXX) with a corresponding blending factor ([**D3DBLEND**](./d3dblend.md)).</span></span> <span data-ttu-id="d54d1-115">Les valeurs de SourceBlend et DestBlend sont comprises entre 0,0 (transparent) et 1,0 (opaque) inclus.</span><span class="sxs-lookup"><span data-stu-id="d54d1-115">The values of SourceBlend and DestBlend range from 0.0 (transparent) to 1.0 (opaque) inclusive.</span></span> <span data-ttu-id="d54d1-116">En outre, une application peut contrôler la transparence d’un pixel en définissant la valeur alpha dans une texture.</span><span class="sxs-lookup"><span data-stu-id="d54d1-116">In addition, an application can control the transparency of a pixel by setting the alpha value in a texture.</span></span> <span data-ttu-id="d54d1-117">Dans ce cas, utilisez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="d54d1-117">In this case, use the following:</span></span>


```
SourceBlend = D3DBLEND_ZERO 
DestBlend = D3DBLEND_ONE
```



<span data-ttu-id="d54d1-118">L’équation de fusion entraîne la transparence du pixel rendu.</span><span class="sxs-lookup"><span data-stu-id="d54d1-118">The blending equation will cause the rendered pixel to be transparent.</span></span> <span data-ttu-id="d54d1-119">Les valeurs par défaut sont :</span><span class="sxs-lookup"><span data-stu-id="d54d1-119">The default values are:</span></span>


```
SourceBlend = D3DBLEND_SRCALPHA 
DestBlend = D3DBLEND_INVSRCALPHA
```



## <a name="related-topics"></a><span data-ttu-id="d54d1-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d54d1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d54d1-121">Fusion de texture</span><span class="sxs-lookup"><span data-stu-id="d54d1-121">Texture Blending</span></span>](texture-blending.md)
</dt> <dt>

[<span data-ttu-id="d54d1-122">Filtrage de texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d54d1-122">Texture Filtering (Direct3D 9)</span></span>](texture-filtering.md)
</dt> <dt>

[<span data-ttu-id="d54d1-123">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="d54d1-123">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
