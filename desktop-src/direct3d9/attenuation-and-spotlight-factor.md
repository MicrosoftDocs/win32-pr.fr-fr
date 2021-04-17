---
description: Les composants d’éclairage diffus et spéculaire de l’équation d’éclairage global contiennent des termes qui décrivent l’atténuation de la lumière et le cône en vedette. Ces termes sont décrits ci-dessous.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Facteur d’atténuation et de focalisation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bb3cb2b1c2a3ee9e0e5d9419ff71dd9a303b6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550821"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a><span data-ttu-id="ffcfa-104">Facteur d’atténuation et de focalisation (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ffcfa-104">Attenuation and Spotlight Factor (Direct3D 9)</span></span>

<span data-ttu-id="ffcfa-105">Les composants d’éclairage diffus et spéculaire de l’équation d’éclairage global contiennent des termes qui décrivent l’atténuation de la lumière et le cône en vedette.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-105">The diffuse and specular lighting components of the global illumination equation contain terms that describe light attenuation and the spotlight cone.</span></span> <span data-ttu-id="ffcfa-106">Ces termes sont décrits ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-106">These terms are described below.</span></span>

## <a name="attenuation"></a><span data-ttu-id="ffcfa-107">Atténuation</span><span class="sxs-lookup"><span data-stu-id="ffcfa-107">Attenuation</span></span>

<span data-ttu-id="ffcfa-108">L’atténuation d’une lumière dépend du type de lumière et de la distance entre la lumière et la position du sommet.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-108">The attenuation of a light depends on the type of light and the distance between the light and the vertex position.</span></span> <span data-ttu-id="ffcfa-109">Pour calculer l’atténuation, utilisez l’une des équations suivantes.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-109">To calculate attenuation, use one of the following equations.</span></span>

<span data-ttu-id="ffcfa-110">Atten = 1/(att0<sub>i</sub> + Att1<sub>i</sub> \* d + att2<sub>i</sub> \* d ²)</span><span class="sxs-lookup"><span data-stu-id="ffcfa-110">Atten = 1/( att0<sub>i</sub> + att1<sub>i</sub> \* d + att2<sub>i</sub> \* d²)</span></span>

<span data-ttu-id="ffcfa-111">Où :</span><span class="sxs-lookup"><span data-stu-id="ffcfa-111">Where:</span></span>



| <span data-ttu-id="ffcfa-112">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ffcfa-112">Parameter</span></span>        | <span data-ttu-id="ffcfa-113">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ffcfa-113">Default value</span></span> | <span data-ttu-id="ffcfa-114">Type</span><span class="sxs-lookup"><span data-stu-id="ffcfa-114">Type</span></span>  | <span data-ttu-id="ffcfa-115">Description</span><span class="sxs-lookup"><span data-stu-id="ffcfa-115">Description</span></span>                                     | <span data-ttu-id="ffcfa-116">Plage</span><span class="sxs-lookup"><span data-stu-id="ffcfa-116">Range</span></span>          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| <span data-ttu-id="ffcfa-117">att0<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="ffcfa-117">att0<sub>i</sub></span></span> | <span data-ttu-id="ffcfa-118">0.0</span><span class="sxs-lookup"><span data-stu-id="ffcfa-118">0.0</span></span>           | <span data-ttu-id="ffcfa-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ffcfa-119">FLOAT</span></span> | <span data-ttu-id="ffcfa-120">Facteur d’atténuation constant</span><span class="sxs-lookup"><span data-stu-id="ffcfa-120">Constant attenuation factor</span></span>                     | <span data-ttu-id="ffcfa-121">0 à + infini</span><span class="sxs-lookup"><span data-stu-id="ffcfa-121">0 to +infinity</span></span> |
| <span data-ttu-id="ffcfa-122">Att1<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="ffcfa-122">att1<sub>i</sub></span></span> | <span data-ttu-id="ffcfa-123">0.0</span><span class="sxs-lookup"><span data-stu-id="ffcfa-123">0.0</span></span>           | <span data-ttu-id="ffcfa-124">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ffcfa-124">FLOAT</span></span> | <span data-ttu-id="ffcfa-125">Facteur d’atténuation linéaire</span><span class="sxs-lookup"><span data-stu-id="ffcfa-125">Linear attenuation factor</span></span>                       | <span data-ttu-id="ffcfa-126">0 à + infini</span><span class="sxs-lookup"><span data-stu-id="ffcfa-126">0 to +infinity</span></span> |
| <span data-ttu-id="ffcfa-127">att2<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="ffcfa-127">att2<sub>i</sub></span></span> | <span data-ttu-id="ffcfa-128">0.0</span><span class="sxs-lookup"><span data-stu-id="ffcfa-128">0.0</span></span>           | <span data-ttu-id="ffcfa-129">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ffcfa-129">FLOAT</span></span> | <span data-ttu-id="ffcfa-130">Facteur d’atténuation quadratique</span><span class="sxs-lookup"><span data-stu-id="ffcfa-130">Quadratic attenuation factor</span></span>                    | <span data-ttu-id="ffcfa-131">0 à + infini</span><span class="sxs-lookup"><span data-stu-id="ffcfa-131">0 to +infinity</span></span> |
| <span data-ttu-id="ffcfa-132">d</span><span class="sxs-lookup"><span data-stu-id="ffcfa-132">d</span></span>                | <span data-ttu-id="ffcfa-133">N/A</span><span class="sxs-lookup"><span data-stu-id="ffcfa-133">N/A</span></span>           | <span data-ttu-id="ffcfa-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ffcfa-134">FLOAT</span></span> | <span data-ttu-id="ffcfa-135">Distance de la position du sommet à la position de la lumière</span><span class="sxs-lookup"><span data-stu-id="ffcfa-135">Distance from vertex position to light position</span></span> | <span data-ttu-id="ffcfa-136">N/A</span><span class="sxs-lookup"><span data-stu-id="ffcfa-136">N/A</span></span>            |



 

-   <span data-ttu-id="ffcfa-137">Atten = 1, si la lumière est une lumière directionnelle.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-137">Atten = 1, if the light is a directional light.</span></span>
-   <span data-ttu-id="ffcfa-138">Atten = 0, si la distance entre la lumière et le vertex est supérieure à la plage de la lumière.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-138">Atten = 0, if the distance between the light and the vertex exceeds the light's range.</span></span>

<span data-ttu-id="ffcfa-139">Les valeurs att0, Att1, att2 sont spécifiées par les membres Attenuation0, Attenuation1 et Attenuation2 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="ffcfa-139">The att0, att1, att2 values are specified by the Attenuation0, Attenuation1, and Attenuation2 members of [**D3DLIGHT9**](d3dlight9.md).</span></span>

<span data-ttu-id="ffcfa-140">La distance entre la lumière et la position du vertex est toujours positive.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-140">The distance between the light and the vertex position is always positive.</span></span>

<span data-ttu-id="ffcfa-141">d = \| L<sub>Rép</sub>\|</span><span class="sxs-lookup"><span data-stu-id="ffcfa-141">d = \| L<sub>dir</sub> \|</span></span>

<span data-ttu-id="ffcfa-142">Où :</span><span class="sxs-lookup"><span data-stu-id="ffcfa-142">Where:</span></span>



| <span data-ttu-id="ffcfa-143">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ffcfa-143">Parameter</span></span>       | <span data-ttu-id="ffcfa-144">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ffcfa-144">Default value</span></span> | <span data-ttu-id="ffcfa-145">Type</span><span class="sxs-lookup"><span data-stu-id="ffcfa-145">Type</span></span>      | <span data-ttu-id="ffcfa-146">Description</span><span class="sxs-lookup"><span data-stu-id="ffcfa-146">Description</span></span>                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <span data-ttu-id="ffcfa-147"><sub>Rép</sub> .</span><span class="sxs-lookup"><span data-stu-id="ffcfa-147">L<sub>dir</sub></span></span> | <span data-ttu-id="ffcfa-148">N/A</span><span class="sxs-lookup"><span data-stu-id="ffcfa-148">N/A</span></span>           | <span data-ttu-id="ffcfa-149">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="ffcfa-149">D3DVECTOR</span></span> | <span data-ttu-id="ffcfa-150">Vecteur de direction de la position du vertex à la position de la lumière</span><span class="sxs-lookup"><span data-stu-id="ffcfa-150">Direction vector from vertex position to the light position</span></span> |



 

<span data-ttu-id="ffcfa-151">Si d est supérieur à la plage de la lumière, autrement dit, le membre de plage d’une structure [**D3DLIGHT9**](d3dlight9.md) , Direct3D n’effectue aucun calcul d’atténuation supplémentaire et n’applique aucun effet de la lumière au vertex.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-151">If d is greater than the light's range, that is, the Range member of a [**D3DLIGHT9**](d3dlight9.md) structure, Direct3D makes no further attenuation calculations and applies no effects from the light to the vertex.</span></span>

<span data-ttu-id="ffcfa-152">Les constantes d’atténuation jouent le rôle de coefficient dans la formule. vous pouvez produire diverses courbes d’atténuation en effectuant des ajustements simples.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-152">The attenuation constants act as coefficients in the formula - you can produce a variety of attenuation curves by making simple adjustments to them.</span></span> <span data-ttu-id="ffcfa-153">Vous pouvez affecter à Attenuation1 la valeur 1,0 pour créer une lumière qui n’est pas atténuée, mais qui est toujours limitée par plage, ou vous pouvez faire des essais avec différentes valeurs pour obtenir divers effets d’atténuation.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-153">You can set Attenuation1 to 1.0 to create a light that doesn't attenuate but is still limited by range, or you can experiment with different values to achieve various attenuation effects.</span></span>

<span data-ttu-id="ffcfa-154">L’atténuation à la plage maximale de la lumière n’est pas 0,0.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-154">The attenuation at the maximum range of the light is not 0.0.</span></span> <span data-ttu-id="ffcfa-155">Pour empêcher l’apparition soudaine de voyants lorsqu’ils sont à l’intervalle de luminosité, une application peut augmenter la plage lumineuse.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-155">To prevent lights from suddenly appearing when they are at the light range, an application can increase the light range.</span></span> <span data-ttu-id="ffcfa-156">Ou bien, l’application peut configurer des constantes d’atténuation afin que le facteur d’atténuation soit proche de 0,0 à la plage lumineuse.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-156">Or, the application can set up attenuation constants so that the attenuation factor is close to 0.0 at the light range.</span></span> <span data-ttu-id="ffcfa-157">La valeur d’atténuation est multipliée par les composants rouge, vert et bleu de la couleur de la lumière pour mettre à l’échelle l’intensité de la lumière en tant que facteur de la lumière de distance se déplace vers un sommet.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-157">The attenuation value is multiplied by the red, green, and blue components of the light's color to scale the light's intensity as a factor of the distance light travels to a vertex.</span></span>

## <a name="spotlight-factor"></a><span data-ttu-id="ffcfa-158">Facteur Gong</span><span class="sxs-lookup"><span data-stu-id="ffcfa-158">Spotlight Factor</span></span>

<span data-ttu-id="ffcfa-159">L’équation suivante spécifie le facteur Spotlight.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-159">The following equation specifies the spotlight factor.</span></span>

![équation du facteur Spotlight](images/dx8light9.png)



| <span data-ttu-id="ffcfa-161">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ffcfa-161">Parameter</span></span>         | <span data-ttu-id="ffcfa-162">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ffcfa-162">Default value</span></span> | <span data-ttu-id="ffcfa-163">Type</span><span class="sxs-lookup"><span data-stu-id="ffcfa-163">Type</span></span>  | <span data-ttu-id="ffcfa-164">Description</span><span class="sxs-lookup"><span data-stu-id="ffcfa-164">Description</span></span>                              | <span data-ttu-id="ffcfa-165">Plage</span><span class="sxs-lookup"><span data-stu-id="ffcfa-165">Range</span></span>                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| <span data-ttu-id="ffcfa-166">Rhô<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="ffcfa-166">rho<sub>i</sub></span></span>   | <span data-ttu-id="ffcfa-167">N/A</span><span class="sxs-lookup"><span data-stu-id="ffcfa-167">N/A</span></span>           | <span data-ttu-id="ffcfa-168">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ffcfa-168">FLOAT</span></span> | <span data-ttu-id="ffcfa-169">cosinus (angle) pour la lumière</span><span class="sxs-lookup"><span data-stu-id="ffcfa-169">cosine(angle) for spotlight i</span></span>            | <span data-ttu-id="ffcfa-170">N/A</span><span class="sxs-lookup"><span data-stu-id="ffcfa-170">N/A</span></span>                      |
| <span data-ttu-id="ffcfa-171">Phi<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="ffcfa-171">phi<sub>i</sub></span></span>   | <span data-ttu-id="ffcfa-172">0.0</span><span class="sxs-lookup"><span data-stu-id="ffcfa-172">0.0</span></span>           | <span data-ttu-id="ffcfa-173">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ffcfa-173">FLOAT</span></span> | <span data-ttu-id="ffcfa-174">Penumbra angle de lumière en radians</span><span class="sxs-lookup"><span data-stu-id="ffcfa-174">Penumbra angle of spotlight i in radians</span></span> | <span data-ttu-id="ffcfa-175">\[thêta<sub>i</sub>, pi)</span><span class="sxs-lookup"><span data-stu-id="ffcfa-175">\[theta<sub>i</sub>, pi)</span></span> |
| <span data-ttu-id="ffcfa-176">thêta<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="ffcfa-176">theta<sub>i</sub></span></span> | <span data-ttu-id="ffcfa-177">0.0</span><span class="sxs-lookup"><span data-stu-id="ffcfa-177">0.0</span></span>           | <span data-ttu-id="ffcfa-178">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ffcfa-178">FLOAT</span></span> | <span data-ttu-id="ffcfa-179">Umbra angle de lumière en radians</span><span class="sxs-lookup"><span data-stu-id="ffcfa-179">Umbra angle of spotlight i in radians</span></span>    | <span data-ttu-id="ffcfa-180">\[0, pi)</span><span class="sxs-lookup"><span data-stu-id="ffcfa-180">\[0, pi)</span></span>                 |
| <span data-ttu-id="ffcfa-181">atténuation</span><span class="sxs-lookup"><span data-stu-id="ffcfa-181">falloff</span></span>           | <span data-ttu-id="ffcfa-182">0.0</span><span class="sxs-lookup"><span data-stu-id="ffcfa-182">0.0</span></span>           | <span data-ttu-id="ffcfa-183">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ffcfa-183">FLOAT</span></span> | <span data-ttu-id="ffcfa-184">Facteur d’atténuation</span><span class="sxs-lookup"><span data-stu-id="ffcfa-184">Falloff factor</span></span>                           | <span data-ttu-id="ffcfa-185">(-infini, + infini)</span><span class="sxs-lookup"><span data-stu-id="ffcfa-185">(-infinity, +infinity)</span></span>   |



 

<span data-ttu-id="ffcfa-186">Où :</span><span class="sxs-lookup"><span data-stu-id="ffcfa-186">Where:</span></span>

<span data-ttu-id="ffcfa-187">Rhô = normal (L<sub>DCS</sub>)<sup>.</sup> normal (L<sub>Rép</sub>)</span><span class="sxs-lookup"><span data-stu-id="ffcfa-187">rho = norm(L<sub>dcs</sub>)<sup>.</sup>norm(L<sub>dir</sub>)</span></span>

<span data-ttu-id="ffcfa-188">et</span><span class="sxs-lookup"><span data-stu-id="ffcfa-188">and:</span></span>



| <span data-ttu-id="ffcfa-189">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ffcfa-189">Parameter</span></span>       | <span data-ttu-id="ffcfa-190">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ffcfa-190">Default value</span></span> | <span data-ttu-id="ffcfa-191">Type</span><span class="sxs-lookup"><span data-stu-id="ffcfa-191">Type</span></span>      | <span data-ttu-id="ffcfa-192">Description</span><span class="sxs-lookup"><span data-stu-id="ffcfa-192">Description</span></span>                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <span data-ttu-id="ffcfa-193">L<sub>DC</sub></span><span class="sxs-lookup"><span data-stu-id="ffcfa-193">L<sub>dcs</sub></span></span> | <span data-ttu-id="ffcfa-194">N/A</span><span class="sxs-lookup"><span data-stu-id="ffcfa-194">N/A</span></span>           | <span data-ttu-id="ffcfa-195">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="ffcfa-195">D3DVECTOR</span></span> | <span data-ttu-id="ffcfa-196">Négatif de la direction de la lumière dans l’espace de l’appareil photo</span><span class="sxs-lookup"><span data-stu-id="ffcfa-196">The negative of the light direction in camera space</span></span>         |
| <span data-ttu-id="ffcfa-197"><sub>Rép</sub> .</span><span class="sxs-lookup"><span data-stu-id="ffcfa-197">L<sub>dir</sub></span></span> | <span data-ttu-id="ffcfa-198">N/A</span><span class="sxs-lookup"><span data-stu-id="ffcfa-198">N/A</span></span>           | <span data-ttu-id="ffcfa-199">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="ffcfa-199">D3DVECTOR</span></span> | <span data-ttu-id="ffcfa-200">Vecteur de direction de la position du vertex à la position de la lumière</span><span class="sxs-lookup"><span data-stu-id="ffcfa-200">Direction vector from vertex position to the light position</span></span> |



 

<span data-ttu-id="ffcfa-201">Après le calcul de l’atténuation légère, Direct3D considère également les effets de Spotlight, le cas échéant, l’angle que la lumière reflète d’une surface et la réflectivité de la matière actuelle pour calculer les composants diffus et spéculaire pour ce vertex.</span><span class="sxs-lookup"><span data-stu-id="ffcfa-201">After computing the light attenuation, Direct3D also considers spotlight effects if applicable, the angle that the light reflects from a surface, and the reflectance of the current material to calculate the diffuse and specular components for that vertex.</span></span> <span data-ttu-id="ffcfa-202">Pour plus d’informations, consultez [Spotlight](light-types.md).</span><span class="sxs-lookup"><span data-stu-id="ffcfa-202">For more information, see [SpotLight](light-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffcfa-203">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ffcfa-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffcfa-204">Mathématiques d’éclairage</span><span class="sxs-lookup"><span data-stu-id="ffcfa-204">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



