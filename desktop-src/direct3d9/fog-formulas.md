---
description: Les applications C++ peuvent contrôler la façon dont le brouillard affecte la couleur des objets dans une scène en modifiant la façon dont Microsoft Direct3D calcule les effets de brouillard sur la distance.
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: Formules de brouillard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75150a00d491f1e3fc1ea1444209449c1c2a825d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846174"
---
# <a name="fog-formulas-direct3d-9"></a><span data-ttu-id="09ca6-103">Formules de brouillard (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="09ca6-103">Fog Formulas (Direct3D 9)</span></span>

<span data-ttu-id="09ca6-104">Les applications C++ peuvent contrôler la façon dont le brouillard affecte la couleur des objets dans une scène en modifiant la façon dont Microsoft Direct3D calcule les effets de brouillard sur la distance.</span><span class="sxs-lookup"><span data-stu-id="09ca6-104">C++ applications can control how fog affects the color of objects in a scene by changing how Microsoft Direct3D computes fog effects over distance.</span></span> <span data-ttu-id="09ca6-105">Le type énuméré [**D3DFOGMODE**](./d3dfogmode.md) contient des membres qui identifient les trois formules de brouillard.</span><span class="sxs-lookup"><span data-stu-id="09ca6-105">The [**D3DFOGMODE**](./d3dfogmode.md) enumerated type contains members that identify the three fog formulas.</span></span> <span data-ttu-id="09ca6-106">Toutes les formules calculent un facteur de brouillard comme fonction de distance, en fonction des paramètres définis par votre application.</span><span class="sxs-lookup"><span data-stu-id="09ca6-106">All formulas calculate a fog factor as a function of distance, given parameters that your application sets.</span></span>

## <a name="linear-fog"></a><span data-ttu-id="09ca6-107">Brouillard linéaire</span><span class="sxs-lookup"><span data-stu-id="09ca6-107">Linear Fog</span></span>

<span data-ttu-id="09ca6-108">Cette valeur est définie avec l' \_ équation linéaire D3DFOG suivante.</span><span class="sxs-lookup"><span data-stu-id="09ca6-108">This is set with the following D3DFOG\_LINEAR equation.</span></span>

![équation du brouillard linéaire Direct3D](images/fogliner.png)

<span data-ttu-id="09ca6-110">where</span><span class="sxs-lookup"><span data-stu-id="09ca6-110">where</span></span>

-   <span data-ttu-id="09ca6-111">Start est la distance à laquelle les effets de brouillard commencent.</span><span class="sxs-lookup"><span data-stu-id="09ca6-111">start is the distance at which fog effects begin.</span></span>
-   <span data-ttu-id="09ca6-112">end est la distance à laquelle les effets de brouillard n’augmentent plus.</span><span class="sxs-lookup"><span data-stu-id="09ca6-112">end is the distance at which fog effects no longer increase.</span></span>
-   <span data-ttu-id="09ca6-113">d représente la profondeur ou la distance à partir du point de vue.</span><span class="sxs-lookup"><span data-stu-id="09ca6-113">d represents depth, or the distance from the viewpoint.</span></span> <span data-ttu-id="09ca6-114">Pour le brouillard basé sur une plage, la valeur de d correspond à la distance entre la position de la caméra et un sommet.</span><span class="sxs-lookup"><span data-stu-id="09ca6-114">For range based fog, the value for d is the distance between the camera position and a vertex.</span></span> <span data-ttu-id="09ca6-115">Pour un brouillard non basé sur une plage, la valeur pour d est la valeur absolue de la coordonnée Z dans l’espace de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="09ca6-115">For non-range based fog, the value for d is the absolute value of the Z-coordinate in camera space.</span></span>

## <a name="exponential-fog"></a><span data-ttu-id="09ca6-116">Brouillard exponentiel</span><span class="sxs-lookup"><span data-stu-id="09ca6-116">Exponential Fog</span></span>

<span data-ttu-id="09ca6-117">Les formules linéaires et exponentielles sont prises en charge pour le brouillard de pixel et le brouillard de vertex.</span><span class="sxs-lookup"><span data-stu-id="09ca6-117">Linear and exponential formulas are supported for both pixel fog and vertex fog.</span></span>

<span data-ttu-id="09ca6-118">Cela est défini avec l’équation D3DFOG \_ exp suivante.</span><span class="sxs-lookup"><span data-stu-id="09ca6-118">This is set with the following D3DFOG\_EXP equation.</span></span>

![équation du brouillard exponentiel Direct3D](images/fogexp.png)

<span data-ttu-id="09ca6-120">where</span><span class="sxs-lookup"><span data-stu-id="09ca6-120">where</span></span>

-   <span data-ttu-id="09ca6-121">e est la base des logarithmes naturels (environ 2,71828).</span><span class="sxs-lookup"><span data-stu-id="09ca6-121">e is the base of natural logarithms (approximately 2.71828).</span></span>
-   <span data-ttu-id="09ca6-122">la densité est une densité de brouillard arbitraire qui peut être comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="09ca6-122">density is an arbitrary fog density that can range from 0.0 to 1.0.</span></span>
-   <span data-ttu-id="09ca6-123">d représente la profondeur, ou la distance par rapport au point de vue, comme indiqué plus haut.</span><span class="sxs-lookup"><span data-stu-id="09ca6-123">d represents depth, or the distance from the viewpoint, as stated earlier.</span></span>

<span data-ttu-id="09ca6-124">Cette valeur est définie avec l' \_ équation D3DFOG EXP2 suivante.</span><span class="sxs-lookup"><span data-stu-id="09ca6-124">This is set with the following D3DFOG\_EXP2 equation.</span></span>

![équation du brouillard exponentielle 2 Direct3D](images/fogexp2.png)

<span data-ttu-id="09ca6-126">where</span><span class="sxs-lookup"><span data-stu-id="09ca6-126">where</span></span>

-   <span data-ttu-id="09ca6-127">e est la base des logarithmes naturels comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="09ca6-127">e is the base of natural logarithms as stated above.</span></span>
-   <span data-ttu-id="09ca6-128">la densité est une densité de brouillard arbitraire qui peut être comprise entre 0,0 et 1,0, comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="09ca6-128">density is an arbitrary fog density that can range from 0.0 to 1.0 as stated above.</span></span>
-   <span data-ttu-id="09ca6-129">d représente la profondeur, ou la distance par rapport au point de vue, comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="09ca6-129">d represents depth, or the distance from the viewpoint, as stated above.</span></span>

> [!Note]  
> <span data-ttu-id="09ca6-130">Le système stocke le facteur de brouillard dans le composant alpha de la couleur spéculaire d’un vertex.</span><span class="sxs-lookup"><span data-stu-id="09ca6-130">The system stores the fog factor in the alpha component of the specular color for a vertex.</span></span> <span data-ttu-id="09ca6-131">Si votre application effectue sa propre transformation et éclairage, vous pouvez insérer des valeurs de facteur de brouillard manuellement, qui seront appliquées par le système lors du rendu.</span><span class="sxs-lookup"><span data-stu-id="09ca6-131">If your application performs its own transformation and lighting, you can insert fog factor values manually, to be applied by the system during rendering.</span></span>

 

<span data-ttu-id="09ca6-132">Le graphique suivant présente ces formules, en utilisant des valeurs communes comme dans les paramètres de formule.</span><span class="sxs-lookup"><span data-stu-id="09ca6-132">The following graph shows these formulas, using common values as in the formula parameters.</span></span>

![graphique des formules de brouillard sur la distance et la quantité de couleur](images/foggraph.png)

<span data-ttu-id="09ca6-134">D3DFOG \_ Linear est 1,0 au début et 0,0 à la fin.</span><span class="sxs-lookup"><span data-stu-id="09ca6-134">D3DFOG\_LINEAR is 1.0 at start and 0.0 at end.</span></span> <span data-ttu-id="09ca6-135">Il n’est pas mesuré par rapport aux plans near ou Far.</span><span class="sxs-lookup"><span data-stu-id="09ca6-135">It is not measured relative to the near or far planes.</span></span>

<span data-ttu-id="09ca6-136">Lorsque Direct3D calcule des effets de brouillard, il utilise le facteur de brouillard de l’une des équations précédentes dans l’équation de fusion suivante.</span><span class="sxs-lookup"><span data-stu-id="09ca6-136">When Direct3D calculates fog effects, it uses the fog factor from one of the preceding equations in the following blending equation.</span></span>

![équation des effets de brouillard pour Direct3D](images/fogcalc.png)

<span data-ttu-id="09ca6-138">Cette formule met effectivement à l’échelle la couleur du polygone actuel par le facteur de brouillard f, puis ajoute le produit à la couleur de brouillard C, mise à l’échelle par l’inverse de l’opération de bits du facteur de brouillard.</span><span class="sxs-lookup"><span data-stu-id="09ca6-138">This formula effectively scales the color of the current polygon C by the fog factor f, and adds the product to the fog color C, scaled by the bitwise inverse of the fog factor.</span></span> <span data-ttu-id="09ca6-139">La valeur de couleur résultante est un mélange de la couleur de brouillard et de la couleur d’origine, en tant que facteur de distance.</span><span class="sxs-lookup"><span data-stu-id="09ca6-139">The resulting color value is a blend of the fog color and the original color, as a factor of distance.</span></span> <span data-ttu-id="09ca6-140">La formule s’applique à tous les appareils pris en charge dans Microsoft DirectX 7,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="09ca6-140">The formula applies to all devices supported in Microsoft DirectX 7.0 and later.</span></span> <span data-ttu-id="09ca6-141">Pour l’appareil rampe héritée, le facteur de brouillard met à l’échelle les composants de couleur diffuse et spéculaire, fixés à la plage 0,0 et 1,0, inclus.</span><span class="sxs-lookup"><span data-stu-id="09ca6-141">For the legacy ramp device, the fog factor scales the diffuse and specular color components, clamped to the range of 0.0 and 1.0, inclusive.</span></span> <span data-ttu-id="09ca6-142">Le facteur de brouillard commence généralement à 1,0 pour le plan proche et diminue à 0,0 du plan lointain.</span><span class="sxs-lookup"><span data-stu-id="09ca6-142">The fog factor typically starts at 1.0 for the near plane and decreases to 0.0 at the far plane.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09ca6-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09ca6-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09ca6-144">Types de brouillard</span><span class="sxs-lookup"><span data-stu-id="09ca6-144">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
