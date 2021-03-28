---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4
description: L’assembleur de nuanceur de pixels est constitué d’un ensemble d’instructions qui fonctionnent sur les données de pixels contenues dans les registres.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 761721a4de64e8a9168bcfea49ce7adf567ea7ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190722"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a><span data-ttu-id="bb33c-103">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="bb33c-103">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4</span></span>

<span data-ttu-id="bb33c-104">L’assembleur de nuanceur de pixels est constitué d’un ensemble d’instructions qui fonctionnent sur les données de pixels contenues dans les registres.</span><span class="sxs-lookup"><span data-stu-id="bb33c-104">The pixel shader assembler is made up of a set of instructions that operate on pixel data contained in registers.</span></span> <span data-ttu-id="bb33c-105">Les opérations sont exprimées en tant qu’instructions composées d’un opérateur et d’un ou plusieurs opérandes.</span><span class="sxs-lookup"><span data-stu-id="bb33c-105">Operations are expressed as instructions comprised of an operator and one or more operands.</span></span> <span data-ttu-id="bb33c-106">Les instructions utilisent des registres pour transférer des données vers et depuis le nuanceur de pixels ALU.</span><span class="sxs-lookup"><span data-stu-id="bb33c-106">Instructions use registers to transfer data in and out of the pixel shader ALU.</span></span> <span data-ttu-id="bb33c-107">Les registres peuvent également être utilisés par certaines instructions pour conserver les résultats temporaires.</span><span class="sxs-lookup"><span data-stu-id="bb33c-107">Registers can also be used by some instructions to hold temporary results.</span></span>

> [!Note]  
> <span data-ttu-id="bb33c-108">La prise en charge de HLSL pour le nuanceur de pixels 1. x est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="bb33c-108">HLSL support for pixel shader 1.x is deprecated.</span></span>

 

## <a name="instructions"></a><span data-ttu-id="bb33c-109">Instructions</span><span class="sxs-lookup"><span data-stu-id="bb33c-109">Instructions</span></span>

<span data-ttu-id="bb33c-110">Il existe deux catégories principales d’instructions de nuanceur de pixels : instructions arithmétiques et instructions d’adressage de texture.</span><span class="sxs-lookup"><span data-stu-id="bb33c-110">There are two main categories of pixel shader instructions: arithmetic instructions and texture addressing instructions.</span></span> <span data-ttu-id="bb33c-111">Les instructions arithmétiques modifient les données de couleur.</span><span class="sxs-lookup"><span data-stu-id="bb33c-111">Arithmetic instructions modify color data.</span></span> <span data-ttu-id="bb33c-112">Les opérations d’adressage de texture traitent les données de coordonnée de texture et, dans la plupart des cas, échantillonnent une texture.</span><span class="sxs-lookup"><span data-stu-id="bb33c-112">Texture addressing operations process texture coordinate data and in most cases, sample a texture.</span></span> <span data-ttu-id="bb33c-113">Les instructions de nuanceur de pixels sont exécutées sur une base par pixel. autrement dit, ils n’ont aucune connaissance d’autres pixels dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="bb33c-113">Pixel shader instructions are run on a per-pixel basis; that is, they have no knowledge of other pixels in the pipeline.</span></span>

<span data-ttu-id="bb33c-114">Les instructions d’adressage de texture consomment chacune un emplacement, mais les instructions arithmétiques peuvent être associées pour activer les composants de couleur (RVB) et une instruction de composant alpha dans un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="bb33c-114">Texture addressing instructions each consume one slot, but arithmetic instructions can be paired to enable both color components (RGB) and an alpha component instruction in a single slot.</span></span>

<span data-ttu-id="bb33c-115">les instructions PS 1 [ \_ \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contiennent une liste des instructions disponibles.</span><span class="sxs-lookup"><span data-stu-id="bb33c-115">[ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contains a list of the available instructions.</span></span>

<span data-ttu-id="bb33c-116">Lorsque l’échantillonnage multiple est activé, les nuanceurs de pixels ne sont exécutés qu’une seule fois par pixel, et non une fois pour chaque sous-pixel.</span><span class="sxs-lookup"><span data-stu-id="bb33c-116">When multisampling is enabled, pixel shaders only get run once per pixel, not once for every subpixel.</span></span> <span data-ttu-id="bb33c-117">L’échantillonnage multiple augmente uniquement la résolution des arêtes de polygones, ainsi que des tests de profondeur et de stencil.</span><span class="sxs-lookup"><span data-stu-id="bb33c-117">Multisampling only increases the resolution of polygon edges, as well as depth and stencil tests.</span></span> <span data-ttu-id="bb33c-118">Par exemple, si l’échantillonnage multiple 3 x 3 est activé et qu’un triangle en cours de pixellisation est trouvé pour couvrir cinq des neuf sous-pixels pour un pixel particulier, le nuanceur de pixels est exécuté une fois et le même résultat de couleur est appliqué aux cinq sous-pixels.</span><span class="sxs-lookup"><span data-stu-id="bb33c-118">For example, if 3x3 multisampling is enabled, and a triangle being rasterized is found to cover five of the nine subpixels for a particular pixel, the pixel shader gets run once and the same color result is applied to all five subpixels.</span></span>

## <a name="registers"></a><span data-ttu-id="bb33c-119">Registres</span><span class="sxs-lookup"><span data-stu-id="bb33c-119">Registers</span></span>

<span data-ttu-id="bb33c-120">[les \_ registres PS 1 1 PS 1 2 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ 3 PS 1 \_ \_ \_ \_ 4](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) répertorient les différents registres utilisés par le nuanceur alu.</span><span class="sxs-lookup"><span data-stu-id="bb33c-120">[ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) lists the different registers used by the shader ALU.</span></span>

## <a name="modifiers"></a><span data-ttu-id="bb33c-121">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="bb33c-121">Modifiers</span></span>

<span data-ttu-id="bb33c-122">Les [modificateurs pour PS \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) peuvent être utilisés pour modifier les fonctionnalités d’une instruction, ou les données lues ou écrites dans un registre.</span><span class="sxs-lookup"><span data-stu-id="bb33c-122">[Modifiers for ps\_1\_X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) can be used to change the functionality of an instruction, or the data read from or written to a register.</span></span>

<span data-ttu-id="bb33c-123">Direct3D 9 requiert des calculs intermédiaires pour maintenir une précision d’au moins 8 bits pour tous les formats de surface.</span><span class="sxs-lookup"><span data-stu-id="bb33c-123">Direct3D 9 requires intermediate computations to maintain at least 8-bit precision for all surface formats.</span></span> <span data-ttu-id="bb33c-124">Il est recommandé d’avoir à la fois une plus grande précision (12 bits) pour les mathématiques en cours et une saturation de 8 bits entre les différentes étapes de texture.</span><span class="sxs-lookup"><span data-stu-id="bb33c-124">Both higher precision (12-bit) for in-stage math, and saturation to 8-bits between texture stages are recommended.</span></span> <span data-ttu-id="bb33c-125">Aucun mode d’arrondi ou exception modifiable n’est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bb33c-125">No modifiable rounding modes or exceptions are supported.</span></span> <span data-ttu-id="bb33c-126">La multiplication doit être prise en charge avec une précision d’arrondi à la valeur la plus proche pour limiter la perte de précision à un minimum.</span><span class="sxs-lookup"><span data-stu-id="bb33c-126">Multiplication should be supported with a round-to-nearest precision to keep precision loss to a minimum.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="bb33c-127">Nombre d’échantillonneurs</span><span class="sxs-lookup"><span data-stu-id="bb33c-127">Sampler Count</span></span>

<span data-ttu-id="bb33c-128">Le nombre d’échantillonneurs de texture disponibles est le suivant :</span><span class="sxs-lookup"><span data-stu-id="bb33c-128">The number of texture samplers available is:</span></span>

-   <span data-ttu-id="bb33c-129">Pour PS \_ 1 \_ 0-PS \_ 1 \_ 3, la valeur maximale est 4.</span><span class="sxs-lookup"><span data-stu-id="bb33c-129">For ps\_1\_0 - ps\_1\_3, the maximum is 4.</span></span>
-   <span data-ttu-id="bb33c-130">Pour PS \_ 1 \_ 4, la valeur maximale est 6.</span><span class="sxs-lookup"><span data-stu-id="bb33c-130">For ps\_1\_4, the maximum is 6.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb33c-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bb33c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb33c-132">Nuanceurs de pixels</span><span class="sxs-lookup"><span data-stu-id="bb33c-132">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




