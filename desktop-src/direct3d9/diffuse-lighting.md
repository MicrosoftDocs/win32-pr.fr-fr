---
description: Après avoir ajusté l’intensité lumineuse pour tout effet d’atténuation, le moteur d’éclairage calcule la quantité de lumière restante à partir d’un vertex, en fonction de l’angle de la normale du vertex et de la direction du feu incident.
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: Lumière diffuse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51e45093786348aaa115ec38c420acec471f718
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108418"
---
# <a name="diffuse-lighting-direct3d-9"></a><span data-ttu-id="21540-103">Lumière diffuse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="21540-103">Diffuse Lighting (Direct3D 9)</span></span>

<span data-ttu-id="21540-104">Après avoir ajusté l’intensité lumineuse pour tout effet d’atténuation, le moteur d’éclairage calcule la quantité de lumière restante à partir d’un vertex, en fonction de l’angle de la normale du vertex et de la direction du feu incident.</span><span class="sxs-lookup"><span data-stu-id="21540-104">After adjusting the light intensity for any attenuation effects, the lighting engine computes how much of the remaining light reflects from a vertex, given the angle of the vertex normal and the direction of the incident light.</span></span> <span data-ttu-id="21540-105">Le moteur d’éclairage passe à cette étape pour les lumières directionnelles, car elles n’atténuent pas les distances.</span><span class="sxs-lookup"><span data-stu-id="21540-105">The lighting engine skips to this step for directional lights because they do not attenuate over distance.</span></span> <span data-ttu-id="21540-106">Le système considère deux types de réflexion, diffus et spéculaire, et utilise une formule différente pour déterminer la quantité de lumière reflétée pour chacun.</span><span class="sxs-lookup"><span data-stu-id="21540-106">The system considers two reflection types, diffuse and specular, and uses a different formula to determine how much light is reflected for each.</span></span> <span data-ttu-id="21540-107">Après avoir calculé les quantités de lumière réfléchie, Direct3D applique ces nouvelles valeurs aux propriétés de réflectivité diffuse et spéculaire du matériau actuel.</span><span class="sxs-lookup"><span data-stu-id="21540-107">After calculating the amounts of light reflected, Direct3D applies these new values to the diffuse and specular reflectance properties of the current material.</span></span> <span data-ttu-id="21540-108">Les valeurs de couleur résultantes sont les composants diffus et spéculaire utilisés par le rastériseur pour produire un ombrage Gouraud et une mise en surbrillance spéculaire.</span><span class="sxs-lookup"><span data-stu-id="21540-108">The resulting color values are the diffuse and specular components that the rasterizer uses to produce Gouraud shading and specular highlighting.</span></span>

<span data-ttu-id="21540-109">L’éclairage diffus est décrit par l’équation suivante.</span><span class="sxs-lookup"><span data-stu-id="21540-109">Diffuse lighting is described by the following equation.</span></span>

<span data-ttu-id="21540-110">Éclairage diffus = somme \[ C<sub>d</sub> \* L<sub>d</sub> \* (N<sup>.</sup> L<sub>Rép</sub>) \* atten \*\]</span><span class="sxs-lookup"><span data-stu-id="21540-110">Diffuse Lighting = sum\[C<sub>d</sub>\*L<sub>d</sub>\*(N<sup>.</sup>L<sub>dir</sub>)\*Atten\*Spot\]</span></span>



| <span data-ttu-id="21540-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="21540-111">Parameter</span></span>       | <span data-ttu-id="21540-112">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="21540-112">Default value</span></span> | <span data-ttu-id="21540-113">Type</span><span class="sxs-lookup"><span data-stu-id="21540-113">Type</span></span>          | <span data-ttu-id="21540-114">Description</span><span class="sxs-lookup"><span data-stu-id="21540-114">Description</span></span>                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21540-115">Sum</span><span class="sxs-lookup"><span data-stu-id="21540-115">sum</span></span>             | <span data-ttu-id="21540-116">N/A</span><span class="sxs-lookup"><span data-stu-id="21540-116">N/A</span></span>           | <span data-ttu-id="21540-117">N/A</span><span class="sxs-lookup"><span data-stu-id="21540-117">N/A</span></span>           | <span data-ttu-id="21540-118">Somme du composant de diffusion de chaque lumière.</span><span class="sxs-lookup"><span data-stu-id="21540-118">Summation of each light's diffuse component.</span></span>                                                                  |
| <span data-ttu-id="21540-119">C<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="21540-119">C<sub>d</sub></span></span>   | <span data-ttu-id="21540-120">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="21540-120">(0,0,0,0)</span></span>     | <span data-ttu-id="21540-121">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="21540-121">D3DCOLORVALUE</span></span> | <span data-ttu-id="21540-122">Couleur diffuse.</span><span class="sxs-lookup"><span data-stu-id="21540-122">Diffuse color.</span></span>                                                                                                |
| <span data-ttu-id="21540-123">L<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="21540-123">L<sub>d</sub></span></span>   | <span data-ttu-id="21540-124">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="21540-124">(0,0,0,0)</span></span>     | <span data-ttu-id="21540-125">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="21540-125">D3DCOLORVALUE</span></span> | <span data-ttu-id="21540-126">Couleur diffuse de la lumière.</span><span class="sxs-lookup"><span data-stu-id="21540-126">Light diffuse color.</span></span>                                                                                          |
| <span data-ttu-id="21540-127">N</span><span class="sxs-lookup"><span data-stu-id="21540-127">N</span></span>               | <span data-ttu-id="21540-128">N/A</span><span class="sxs-lookup"><span data-stu-id="21540-128">N/A</span></span>           | <span data-ttu-id="21540-129">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="21540-129">D3DVECTOR</span></span>     | <span data-ttu-id="21540-130">Vertex-normal</span><span class="sxs-lookup"><span data-stu-id="21540-130">Vertex normal</span></span>                                                                                                 |
| <span data-ttu-id="21540-131"><sub>Rép</sub> .</span><span class="sxs-lookup"><span data-stu-id="21540-131">L<sub>dir</sub></span></span> | <span data-ttu-id="21540-132">N/A</span><span class="sxs-lookup"><span data-stu-id="21540-132">N/A</span></span>           | <span data-ttu-id="21540-133">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="21540-133">D3DVECTOR</span></span>     | <span data-ttu-id="21540-134">Vecteur de direction du sommet de l’objet à la lumière.</span><span class="sxs-lookup"><span data-stu-id="21540-134">Direction vector from object vertex to the light.</span></span>                                                             |
| <span data-ttu-id="21540-135">Atten</span><span class="sxs-lookup"><span data-stu-id="21540-135">Atten</span></span>           | <span data-ttu-id="21540-136">N/A</span><span class="sxs-lookup"><span data-stu-id="21540-136">N/A</span></span>           | <span data-ttu-id="21540-137">FLOAT</span><span class="sxs-lookup"><span data-stu-id="21540-137">FLOAT</span></span>         | <span data-ttu-id="21540-138">Atténuation de la lumière.</span><span class="sxs-lookup"><span data-stu-id="21540-138">Light attenuation.</span></span> <span data-ttu-id="21540-139">Consultez [facteur d’atténuation et de focalisation (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="21540-139">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="21540-140">Zone</span><span class="sxs-lookup"><span data-stu-id="21540-140">Spot</span></span>            | <span data-ttu-id="21540-141">N/A</span><span class="sxs-lookup"><span data-stu-id="21540-141">N/A</span></span>           | <span data-ttu-id="21540-142">FLOAT</span><span class="sxs-lookup"><span data-stu-id="21540-142">FLOAT</span></span>         | <span data-ttu-id="21540-143">Facteur Gong.</span><span class="sxs-lookup"><span data-stu-id="21540-143">Spotlight factor.</span></span> <span data-ttu-id="21540-144">Consultez [facteur d’atténuation et de focalisation (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="21540-144">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>  |



 

<span data-ttu-id="21540-145">La valeur de C<sub>d</sub> est :</span><span class="sxs-lookup"><span data-stu-id="21540-145">The value for C<sub>d</sub> is either:</span></span>

-   <span data-ttu-id="21540-146">Sommet color1, si DIFFUSEMATERIALSOURCE = D3DMCS \_ color1, et la première couleur de vertex est fournie dans la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="21540-146">vertex color1, if DIFFUSEMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="21540-147">le sommet color2, si DIFFUSEMATERIALSOURCE = D3DMCS \_ color2, et la deuxième couleur du vertex sont fournies dans la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="21540-147">vertex color2, if DIFFUSEMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="21540-148">couleur diffuse de matériau</span><span class="sxs-lookup"><span data-stu-id="21540-148">material diffuse color</span></span>

> [!Note]  
> <span data-ttu-id="21540-149">Si l’une des options DIFFUSEMATERIALSOURCE est utilisée et que la couleur du vertex n’est pas fournie, la couleur de diffusion matérielle est utilisée.</span><span class="sxs-lookup"><span data-stu-id="21540-149">If either DIFFUSEMATERIALSOURCE option is used, and the vertex color is not provided, the material diffuse color is used.</span></span>

 

<span data-ttu-id="21540-150">Pour calculer l’atténuation (atten) ou les caractéristiques de Spotlight (spot), consultez [facteur d’atténuation et de projecteur (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="21540-150">To calculate the attenuation (Atten) or the spotlight characteristics (Spot), see [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>

<span data-ttu-id="21540-151">Les Composants diffuses sont ancrés de 0 à 255, après que toutes les lumières ont été traitées et interpolées séparément.</span><span class="sxs-lookup"><span data-stu-id="21540-151">Diffuse components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span> <span data-ttu-id="21540-152">La valeur d’éclairage diffus résultante est une combinaison des valeurs de lumière ambiante, diffuse et émissif.</span><span class="sxs-lookup"><span data-stu-id="21540-152">The resulting diffuse lighting value is a combination of the ambient, diffuse and emissive light values.</span></span>

## <a name="example"></a><span data-ttu-id="21540-153">Exemple</span><span class="sxs-lookup"><span data-stu-id="21540-153">Example</span></span>

<span data-ttu-id="21540-154">Dans cet exemple, l’objet est coloré à l’aide de la couleur lumière diffuse et d’une couleur diffuse de matériau.</span><span class="sxs-lookup"><span data-stu-id="21540-154">In this example, the object is colored using the light diffuse color and a material diffuse color.</span></span> <span data-ttu-id="21540-155">Le code est illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="21540-155">The code is shown below.</span></span>


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

// set directional light diffuse color
light.Diffuse.r = 1.0f;
light.Diffuse.g = 1.0f;
light.Diffuse.b = 1.0f;
light.Diffuse.a = 1.0f;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );

// if a material is used, SetRenderState must be used
// vertex color = light diffuse color * material diffuse color
mtrl.Diffuse.r = 0.75f;
mtrl.Diffuse.g = 0.0f;
mtrl.Diffuse.b = 0.0f;
mtrl.Diffuse.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="21540-156">D’après l’équation, la couleur résultante pour les vertex d’objet est une combinaison de la couleur de l’élément et de la couleur claire.</span><span class="sxs-lookup"><span data-stu-id="21540-156">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="21540-157">Les deux illustrations suivantes affichent la couleur de matériau, grise, et la couleur claire, qui est brillante rouge.</span><span class="sxs-lookup"><span data-stu-id="21540-157">The following two illustrations show the material color, which is gray, and the light color, which is bright red.</span></span>

![illustration d’une sphère grise](images/amb1.jpg)![illustration d’une sphère rouge](images/lightred.jpg)

<span data-ttu-id="21540-160">La scène qui en résulte est présentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="21540-160">The resulting scene is shown in the following illustration.</span></span> <span data-ttu-id="21540-161">Le seul objet de la scène est une sphère.</span><span class="sxs-lookup"><span data-stu-id="21540-161">The only object in the scene is a sphere.</span></span> <span data-ttu-id="21540-162">Le calcul de l’éclairage diffus prend la couleur diffuse de la lumière et du matériau, et le modifie selon l’angle entre la direction de la lumière et le sommet normal à l’aide du point.</span><span class="sxs-lookup"><span data-stu-id="21540-162">The diffuse lighting calculation takes the material and light diffuse color and modifies it by the angle between the light direction and the vertex normal using the dot product.</span></span> <span data-ttu-id="21540-163">Par conséquent, le verso de la sphère est plus sombre lorsque la surface de la sphère est éloignée de la lumière.</span><span class="sxs-lookup"><span data-stu-id="21540-163">As a result, the backside of the sphere gets darker as the surface of the sphere curves away from the light.</span></span>

![illustration d’une sphère avec éclairage diffus](images/lightd.jpg)

<span data-ttu-id="21540-165">En associant l’éclairage diffus à l’éclairage ambiant de l’exemple précédent, la surface entière de l’objet est dégradée.</span><span class="sxs-lookup"><span data-stu-id="21540-165">Combining the diffuse lighting with the ambient lighting from the previous example shades the entire surface of the object.</span></span> <span data-ttu-id="21540-166">La lumière ambiante dégrade la surface entière et la lumière diffuse permet de révéler la forme 3D de l’objet, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="21540-166">The ambient light shades the entire surface and the diffuse light helps reveal the object's 3D shape, as shown in the following illustration.</span></span>

![illustration d’une sphère avec éclairage diffus et éclairage ambiant](images/lightad.jpg)

<span data-ttu-id="21540-168">L’éclairage diffus est plus gourmand en calcul que l’éclairage ambiant.</span><span class="sxs-lookup"><span data-stu-id="21540-168">Diffuse lighting is more intensive to calculate than ambient lighting.</span></span> <span data-ttu-id="21540-169">Étant donné qu’elle dépend des normales aux sommets et de la direction de la lumière, vous pouvez voir la géométrie des objets dans l’espace 3D, ce qui produit un éclairage plus réaliste que l’éclairage ambiant.</span><span class="sxs-lookup"><span data-stu-id="21540-169">Because it depends on the vertex normals and light direction, you can see the objects geometry in 3D space, which produces a more realistic lighting than ambient lighting.</span></span> <span data-ttu-id="21540-170">Vous pouvez utiliser des surbrillances spéculaires pour obtenir une apparence plus réaliste.</span><span class="sxs-lookup"><span data-stu-id="21540-170">You can use specular highlights to achieve a more realistic look.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21540-171">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="21540-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21540-172">Mathématiques d’éclairage</span><span class="sxs-lookup"><span data-stu-id="21540-172">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



