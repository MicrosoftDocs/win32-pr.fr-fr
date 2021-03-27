---
title: Décalage de profondeur
description: Les polygones en espace 3D peuvent être affichés comme s’ils n’étaient pas coplanés en ajoutant un biais (ou un biais de profondeur) à chacun d’eux.
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6f9a3850b03e033a90b358d0c6ffd1ceef830f
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734933"
---
# <a name="depth-bias"></a><span data-ttu-id="63712-103">Décalage de profondeur</span><span class="sxs-lookup"><span data-stu-id="63712-103">Depth Bias</span></span>

<span data-ttu-id="63712-104">Les polygones en espace 3D peuvent être affichés comme s’ils n’étaient pas coplanés en ajoutant un biais (ou un biais de profondeur) à chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="63712-104">Polygons that are coplanar in 3D space can be made to appear as if they are not coplanar by adding a z-bias (or depth bias) to each one.</span></span>

<span data-ttu-id="63712-105">Il s’agit d’une technique couramment utilisée pour s’assurer que les ombres d’une scène s’affichent correctement.</span><span class="sxs-lookup"><span data-stu-id="63712-105">This is a technique commonly used to ensure that shadows in a scene are displayed properly.</span></span> <span data-ttu-id="63712-106">Par exemple, une ombre sur un mur aura probablement la même valeur de profondeur que le mur.</span><span class="sxs-lookup"><span data-stu-id="63712-106">For instance, a shadow on a wall will likely have the same depth value as the wall.</span></span> <span data-ttu-id="63712-107">Si une application affiche d’abord un mur, puis une ombre, l’ombre peut ne pas être visible ou les artefacts de profondeur peuvent être visibles.</span><span class="sxs-lookup"><span data-stu-id="63712-107">If an application renders a wall first and then a shadow, the shadow might not be visible, or depth artifacts might be visible.</span></span>


<span data-ttu-id="63712-108">Une application peut aider à s’assurer que les polygones sont rendus correctement en ajoutant le biais (à partir du membre **DepthBias** de [**d3d11 \_ rastériseur \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) aux valeurs z que le système utilise lors du rendu des jeux de polygones coplanaires.</span><span class="sxs-lookup"><span data-stu-id="63712-108">An application can help ensure that coplanar polygons are rendered properly by adding the bias (from the **DepthBias** member of [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) to the z-values that the system uses when rendering the sets of coplanar polygons.</span></span> <span data-ttu-id="63712-109">Les polygones avec une plus grande valeur z sont dessinés devant les polygones avec une plus petite valeur z.</span><span class="sxs-lookup"><span data-stu-id="63712-109">Polygons with a larger z value will be drawn in front of polygons with a smaller z value.</span></span>

<span data-ttu-id="63712-110">Il existe deux options pour calculer le décalage de profondeur.</span><span class="sxs-lookup"><span data-stu-id="63712-110">There are two options for calculating depth bias.</span></span>

1.  <span data-ttu-id="63712-111">Si la mémoire tampon de profondeur actuellement liée à l’étape de fusion de sortie a un format **UNORM** ou qu’aucun tampon de profondeur n’est lié, la valeur d’écart est calculée comme suit :</span><span class="sxs-lookup"><span data-stu-id="63712-111">If the depth buffer currently bound to the output-merger stage has a **UNORM** format or no depth buffer is bound, the bias value is calculated like this:</span></span>
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    <span data-ttu-id="63712-112">où *r* est la valeur représentable minimale > 0 dans le format de mémoire tampon de profondeur converti en **float32**.</span><span class="sxs-lookup"><span data-stu-id="63712-112">where *r* is the minimum representable value > 0 in the depth-buffer format converted to **float32**.</span></span> <span data-ttu-id="63712-113">Les valeurs **DepthBias** et **SlopeScaledDepthBias** sont des membres de structure [**d3d11 \_ rastériseur \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) .</span><span class="sxs-lookup"><span data-stu-id="63712-113">The **DepthBias** and **SlopeScaledDepthBias** values are [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) structure members.</span></span> <span data-ttu-id="63712-114">La valeur de **MaxDepthSlope** est le maximum des pentes horizontales et verticales de la valeur de profondeur au pixel.</span><span class="sxs-lookup"><span data-stu-id="63712-114">The **MaxDepthSlope** value is the maximum of the horizontal and vertical slopes of the depth value at the pixel.</span></span>
2.  <span data-ttu-id="63712-115">Si une mémoire tampon de profondeur à virgule flottante est liée à l’étape de fusion de sortie, la valeur de décalage est calculée comme suit :</span><span class="sxs-lookup"><span data-stu-id="63712-115">If a floating-point depth buffer is bound to the output-merger stage the bias value is calculated like this:</span></span>
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    <span data-ttu-id="63712-116">où *r* est le nombre de bits de mantisse dans la représentation à virgule flottante (à l’exclusion du bit masqué); par exemple, 23 pour **float32**.</span><span class="sxs-lookup"><span data-stu-id="63712-116">where *r* is the number of mantissa bits in the floating point representation (excluding the hidden bit); for example, 23 for **float32**.</span></span>

<span data-ttu-id="63712-117">La valeur de biais est ensuite ancrée comme suit :</span><span class="sxs-lookup"><span data-stu-id="63712-117">The bias value is then clamped like this:</span></span>


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



<span data-ttu-id="63712-118">La valeur de biais est ensuite utilisée pour calculer la profondeur de pixel.</span><span class="sxs-lookup"><span data-stu-id="63712-118">The bias value is then used to calculate the pixel depth.</span></span>


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



<span data-ttu-id="63712-119">Les opérations de décalage de profondeur se produisent sur les sommets après le découpage. par conséquent, l’écart de profondeur n’a aucun effet sur le découpage géométrique.</span><span class="sxs-lookup"><span data-stu-id="63712-119">Depth-bias operations occur on vertices after clipping, therefore, depth-bias has no effect on geometric clipping.</span></span> <span data-ttu-id="63712-120">La valeur de biais est constante pour une primitive donnée et est ajoutée à la valeur z pour chaque vertex avant l’installation de l’interpolateur.</span><span class="sxs-lookup"><span data-stu-id="63712-120">The bias value is constant for a given primitive and is added to the z value for each vertex before interpolator setup.</span></span> <span data-ttu-id="63712-121">Lorsque vous utilisez les [niveaux de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 et supérieurs, tous les calculs de biais sont effectués à l’aide de l’arithmétique à virgule flottante 32 bits.</span><span class="sxs-lookup"><span data-stu-id="63712-121">When you use [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 10.0 and higher, all bias calculations are performed using 32-bit floating-point arithmetic.</span></span> <span data-ttu-id="63712-122">Le biais n’est appliqué à aucune primitive de point ou de ligne, à l’exception des lignes dessinées en mode filaire.</span><span class="sxs-lookup"><span data-stu-id="63712-122">Bias is not applied to any point or line primitives, except for lines drawn in wireframe mode.</span></span>

<span data-ttu-id="63712-123">L’un des artefacts avec des ombres basées sur une mémoire tampon Shadow est l’acné Shadow, ou un ombrage de surface lui-même en raison de différences mineures entre le calcul de profondeur dans un nuanceur et la profondeur de la même surface dans le tampon d’ombre.</span><span class="sxs-lookup"><span data-stu-id="63712-123">One of the artifacts with shadow buffer based shadows is shadow acne, or a surface shadowing itself due to minor differences between the depth computation in a shader, and the depth of the same surface in the shadow buffer.</span></span> <span data-ttu-id="63712-124">Pour pallier cela, vous pouvez utiliser **DepthBias** et **SlopeScaledDepthBias** lors du rendu d’une mémoire tampon d’ombre.</span><span class="sxs-lookup"><span data-stu-id="63712-124">One way to alleviate this is to use **DepthBias** and **SlopeScaledDepthBias** when rendering a shadow buffer.</span></span> <span data-ttu-id="63712-125">L’idée est de pousser des surfaces suffisamment en arrière lors du rendu d’un tampon d’ombre afin que le résultat de la comparaison (entre le tampon d’ombre z et le nuanceur z) soit cohérent sur l’aire de conception et éviter l’auto-ombrage local.</span><span class="sxs-lookup"><span data-stu-id="63712-125">The idea is to push surfaces out enough while rendering a shadow buffer so that the comparison result (between the shadow buffer z and the shader z) is consistent across the surface, and avoid local self-shadowing.</span></span>

<span data-ttu-id="63712-126">Toutefois, l’utilisation de **DepthBias** et de **SlopeScaledDepthBias** peut introduire de nouveaux problèmes de rendu lorsqu’un polygone affiché à un angle extrêmement aigu fait que l’équation de décalage génère une très grande valeur z.</span><span class="sxs-lookup"><span data-stu-id="63712-126">However, using **DepthBias** and **SlopeScaledDepthBias** can introduce new rendering problems when a polygon viewed at an extremely sharp angle causes the bias equation to generate a very large z value.</span></span> <span data-ttu-id="63712-127">En effet, cela pousse le polygone extrêmement loin de la surface d’origine dans le mappage d’ombre.</span><span class="sxs-lookup"><span data-stu-id="63712-127">This in effect pushes the polygon extremely far away from the original surface in the shadow map.</span></span> <span data-ttu-id="63712-128">L’une des méthodes permettant d’atténuer ce problème consiste à utiliser **DepthBiasClamp**, qui fournit une limite supérieure (positive ou négative) sur la grandeur de l’écart z calculé.</span><span class="sxs-lookup"><span data-stu-id="63712-128">One way to help alleviate this particular problem is to use **DepthBiasClamp**, which provides an upper bound (positive or negative) on the magnitude of the z bias calculated.</span></span>

> [!Note]  
> <span data-ttu-id="63712-129">Pour les [niveaux de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) 9,1, 9,2, 9,3, **DepthBiasClamp** n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="63712-129">For [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 9.1, 9.2, 9.3, **DepthBiasClamp** is not supported.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="63712-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63712-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63712-131">Sortie-étape de fusion</span><span class="sxs-lookup"><span data-stu-id="63712-131">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




