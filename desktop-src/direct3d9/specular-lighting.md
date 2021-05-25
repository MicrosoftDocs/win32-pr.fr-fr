---
description: La modélisation de la réflexion spéculaire nécessite que le système sache non seulement dans quel sens le feu est en déplacement, mais également dans la direction de l’oeil du spectateur.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Éclairage spéculaire (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b16d71bd8d814e104cf8a90d1d1fe9b15ba10f3
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343674"
---
# <a name="specular-lighting-direct3d-9"></a><span data-ttu-id="c65f9-103">Éclairage spéculaire (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c65f9-103">Specular Lighting (Direct3D 9)</span></span>

<span data-ttu-id="c65f9-104">La modélisation de la réflexion spéculaire nécessite que le système sache non seulement dans quel sens le feu est en déplacement, mais également dans la direction de l’oeil du spectateur.</span><span class="sxs-lookup"><span data-stu-id="c65f9-104">Modeling specular reflection requires that the system not only know in what direction light is traveling, but also the direction to the viewer's eye.</span></span> <span data-ttu-id="c65f9-105">Le système utilise une version simplifiée du modèle de réflexion spéculaire Phong, qui utilise un vecteur à mi-chemin pour rapprocher l’intensité de la réflexion spéculaire.</span><span class="sxs-lookup"><span data-stu-id="c65f9-105">The system uses a simplified version of the Phong specular-reflection model, which employs a halfway vector to approximate the intensity of specular reflection.</span></span>

<span data-ttu-id="c65f9-106">L’état d’éclairage par défaut ne calcule pas les surbrillances spéculaires.</span><span class="sxs-lookup"><span data-stu-id="c65f9-106">The default lighting state does not calculate specular highlights.</span></span> <span data-ttu-id="c65f9-107">Pour activer l’éclairage spéculaire, veillez à définir D3DRS \_ SpecularEnable sur **true**.</span><span class="sxs-lookup"><span data-stu-id="c65f9-107">To enable specular lighting, be sure to set D3DRS\_SPECULARENABLE to **TRUE**.</span></span>

## <a name="specular-lighting-equation"></a><span data-ttu-id="c65f9-108">Équation d’éclairage spéculaire</span><span class="sxs-lookup"><span data-stu-id="c65f9-108">Specular Lighting Equation</span></span>

<span data-ttu-id="c65f9-109">L’éclairage spéculaire est décrit par l’équation suivante :</span><span class="sxs-lookup"><span data-stu-id="c65f9-109">Specular Lighting is described by the following equation:</span></span>

<span data-ttu-id="c65f9-110">**Éclairage spéculaire = cs \* Sum \[ ls \* (N · H)<sup>P</sup> \* atten \*\]**</span><span class="sxs-lookup"><span data-stu-id="c65f9-110">**Specular Lighting = Cₛ \* sum\[Lₛ \* (N · H)<sup>P</sup> \* Atten \* Spot\]**</span></span>



 

<span data-ttu-id="c65f9-111">Le tableau suivant identifie les variables, leurs types et leurs plages.</span><span class="sxs-lookup"><span data-stu-id="c65f9-111">The following table identifies the variables, their types, and their ranges.</span></span>



| <span data-ttu-id="c65f9-112">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c65f9-112">Parameter</span></span>    | <span data-ttu-id="c65f9-113">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c65f9-113">Default value</span></span> | <span data-ttu-id="c65f9-114">Type</span><span class="sxs-lookup"><span data-stu-id="c65f9-114">Type</span></span>          | <span data-ttu-id="c65f9-115">Description</span><span class="sxs-lookup"><span data-stu-id="c65f9-115">Description</span></span>                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c65f9-116">C</span><span class="sxs-lookup"><span data-stu-id="c65f9-116">Cₛ</span></span>           | <span data-ttu-id="c65f9-117">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="c65f9-117">(0,0,0,0)</span></span>     | <span data-ttu-id="c65f9-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="c65f9-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="c65f9-119">Couleur spéculaire.</span><span class="sxs-lookup"><span data-stu-id="c65f9-119">Specular color.</span></span>                                                                                                     |
| <span data-ttu-id="c65f9-120">Sum</span><span class="sxs-lookup"><span data-stu-id="c65f9-120">sum</span></span>          | <span data-ttu-id="c65f9-121">N/A</span><span class="sxs-lookup"><span data-stu-id="c65f9-121">N/A</span></span>           | <span data-ttu-id="c65f9-122">N/A</span><span class="sxs-lookup"><span data-stu-id="c65f9-122">N/A</span></span>           | <span data-ttu-id="c65f9-123">Somme du composant spéculaire de chaque lumière.</span><span class="sxs-lookup"><span data-stu-id="c65f9-123">Summation of each light's specular component.</span></span>                                                                       |
| <span data-ttu-id="c65f9-124">N</span><span class="sxs-lookup"><span data-stu-id="c65f9-124">N</span></span>            | <span data-ttu-id="c65f9-125">N/A</span><span class="sxs-lookup"><span data-stu-id="c65f9-125">N/A</span></span>           | <span data-ttu-id="c65f9-126">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="c65f9-126">D3DVECTOR</span></span>     | <span data-ttu-id="c65f9-127">Normale au vertex.</span><span class="sxs-lookup"><span data-stu-id="c65f9-127">Vertex normal.</span></span>                                                                                                      |
| <span data-ttu-id="c65f9-128">H</span><span class="sxs-lookup"><span data-stu-id="c65f9-128">H</span></span>            | <span data-ttu-id="c65f9-129">N/A</span><span class="sxs-lookup"><span data-stu-id="c65f9-129">N/A</span></span>           | <span data-ttu-id="c65f9-130">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="c65f9-130">D3DVECTOR</span></span>     | <span data-ttu-id="c65f9-131">Vecteur à demi-sens.</span><span class="sxs-lookup"><span data-stu-id="c65f9-131">Half way vector.</span></span> <span data-ttu-id="c65f9-132">Consultez la section sur le vecteur à mi-chemin.</span><span class="sxs-lookup"><span data-stu-id="c65f9-132">See the section on the halfway vector.</span></span>                                                             |
| <span data-ttu-id="c65f9-133"><sup>P</sup></span><span class="sxs-lookup"><span data-stu-id="c65f9-133"><sup>P</sup></span></span> | <span data-ttu-id="c65f9-134">0.0</span><span class="sxs-lookup"><span data-stu-id="c65f9-134">0.0</span></span>           | <span data-ttu-id="c65f9-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c65f9-135">FLOAT</span></span>         | <span data-ttu-id="c65f9-136">Puissance de réflexion spéculaire.</span><span class="sxs-lookup"><span data-stu-id="c65f9-136">Specular reflection power.</span></span> <span data-ttu-id="c65f9-137">La plage est comprise entre 0 et + infini</span><span class="sxs-lookup"><span data-stu-id="c65f9-137">Range is 0 to +infinity</span></span>                                                                  |
| <span data-ttu-id="c65f9-138">LS</span><span class="sxs-lookup"><span data-stu-id="c65f9-138">Lₛ</span></span>           | <span data-ttu-id="c65f9-139">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="c65f9-139">(0,0,0,0)</span></span>     | <span data-ttu-id="c65f9-140">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="c65f9-140">D3DCOLORVALUE</span></span> | <span data-ttu-id="c65f9-141">Couleur spéculaire clair.</span><span class="sxs-lookup"><span data-stu-id="c65f9-141">Light specular color.</span></span>                                                                                               |
| <span data-ttu-id="c65f9-142">Atten</span><span class="sxs-lookup"><span data-stu-id="c65f9-142">Atten</span></span>        | <span data-ttu-id="c65f9-143">N/A</span><span class="sxs-lookup"><span data-stu-id="c65f9-143">N/A</span></span>           | <span data-ttu-id="c65f9-144">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c65f9-144">FLOAT</span></span>         | <span data-ttu-id="c65f9-145">Valeur d’atténuation de la lumière.</span><span class="sxs-lookup"><span data-stu-id="c65f9-145">Light attenuation value.</span></span> <span data-ttu-id="c65f9-146">Consultez [facteur d’atténuation et de focalisation (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="c65f9-146">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="c65f9-147">Zone</span><span class="sxs-lookup"><span data-stu-id="c65f9-147">Spot</span></span>         | <span data-ttu-id="c65f9-148">N/A</span><span class="sxs-lookup"><span data-stu-id="c65f9-148">N/A</span></span>           | <span data-ttu-id="c65f9-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="c65f9-149">FLOAT</span></span>         | <span data-ttu-id="c65f9-150">Facteur Gong.</span><span class="sxs-lookup"><span data-stu-id="c65f9-150">Spotlight factor.</span></span> <span data-ttu-id="c65f9-151">Consultez [facteur d’atténuation et de focalisation (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="c65f9-151">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>        |



 

<span data-ttu-id="c65f9-152">La valeur de CS est l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="c65f9-152">The value for Cₛ is either:</span></span>


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   <span data-ttu-id="c65f9-153">Sommet color1, si la source de matériau spéculaire est D3DMCS \_ color1, et la première couleur de vertex est fournie dans la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="c65f9-153">vertex color1, if the specular material source is D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="c65f9-154">le vertex color2, si la source de matériau spéculaire est D3DMCS \_ color2, et la deuxième couleur de vertex est fournie dans la déclaration de vertex.</span><span class="sxs-lookup"><span data-stu-id="c65f9-154">vertex color2, if specular material source is D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="c65f9-155">couleur spéculaire</span><span class="sxs-lookup"><span data-stu-id="c65f9-155">material specular color</span></span>

> [!Note]  
> <span data-ttu-id="c65f9-156">Si l’option source de matériau spéculaire est utilisée et que la couleur du vertex n’est pas fournie, la couleur spéculaire est utilisée.</span><span class="sxs-lookup"><span data-stu-id="c65f9-156">If either specular material source option is used and the vertex color is not provided, then the material specular color is used.</span></span>

 

<span data-ttu-id="c65f9-157">Les composants spéculaires sont ancrés à une valeur comprise entre 0 et 255, après que toutes les lumières ont été traitées et interpolées séparément.</span><span class="sxs-lookup"><span data-stu-id="c65f9-157">Specular components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span>

## <a name="the-halfway-vector"></a><span data-ttu-id="c65f9-158">Vecteur à mi-chemin</span><span class="sxs-lookup"><span data-stu-id="c65f9-158">The Halfway Vector</span></span>

<span data-ttu-id="c65f9-159">Le vecteur à mi-chemin (H) existe à mi-chemin entre deux vecteurs : le vecteur d’un sommet d’objet à la source de lumière et le vecteur d’un sommet d’objet à la position de la caméra.</span><span class="sxs-lookup"><span data-stu-id="c65f9-159">The halfway vector (H) exists midway between two vectors: the vector from an object vertex to the light source, and the vector from an object vertex to the camera position.</span></span> <span data-ttu-id="c65f9-160">Direct3D offre deux façons de calculer le vecteur à mi-chemin.</span><span class="sxs-lookup"><span data-stu-id="c65f9-160">Direct3D provides two ways to compute the halfway vector.</span></span> <span data-ttu-id="c65f9-161">Quand D3DRS \_ LOCALVIEWER est défini sur **true**, le système calcule le vecteur à mi-chemin à l’aide de la position de la caméra et la position du vertex, ainsi que le vecteur de direction de la lumière.</span><span class="sxs-lookup"><span data-stu-id="c65f9-161">When D3DRS\_LOCALVIEWER is set to **TRUE**, the system calculates the halfway vector using the position of the camera and the position of the vertex, along with the light's direction vector.</span></span> <span data-ttu-id="c65f9-162">La formule suivante illustre cela.</span><span class="sxs-lookup"><span data-stu-id="c65f9-162">The following formula illustrates this.</span></span>

<span data-ttu-id="c65f9-163">**H = normal (normal (CP-VP) + L <sub>Rép</sub>)**</span><span class="sxs-lookup"><span data-stu-id="c65f9-163">**H = norm(norm(Cₚ - Vₚ) + L<sub>dir</sub>)**</span></span>



 



| <span data-ttu-id="c65f9-164">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c65f9-164">Parameter</span></span>       | <span data-ttu-id="c65f9-165">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c65f9-165">Default value</span></span> | <span data-ttu-id="c65f9-166">Type</span><span class="sxs-lookup"><span data-stu-id="c65f9-166">Type</span></span>      | <span data-ttu-id="c65f9-167">Description</span><span class="sxs-lookup"><span data-stu-id="c65f9-167">Description</span></span>                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| <span data-ttu-id="c65f9-168">CP</span><span class="sxs-lookup"><span data-stu-id="c65f9-168">Cₚ</span></span>              | <span data-ttu-id="c65f9-169">N/A</span><span class="sxs-lookup"><span data-stu-id="c65f9-169">N/A</span></span>           | <span data-ttu-id="c65f9-170">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="c65f9-170">D3DVECTOR</span></span> | <span data-ttu-id="c65f9-171">Position de la caméra.</span><span class="sxs-lookup"><span data-stu-id="c65f9-171">Camera position.</span></span>                                             |
| <span data-ttu-id="c65f9-172">VP</span><span class="sxs-lookup"><span data-stu-id="c65f9-172">Vₚ</span></span>              | <span data-ttu-id="c65f9-173">N/A</span><span class="sxs-lookup"><span data-stu-id="c65f9-173">N/A</span></span>           | <span data-ttu-id="c65f9-174">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="c65f9-174">D3DVECTOR</span></span> | <span data-ttu-id="c65f9-175">Position du vertex.</span><span class="sxs-lookup"><span data-stu-id="c65f9-175">Vertex position.</span></span>                                             |
| <span data-ttu-id="c65f9-176"><sub>Rép</sub> .</span><span class="sxs-lookup"><span data-stu-id="c65f9-176">L<sub>dir</sub></span></span> | <span data-ttu-id="c65f9-177">N/A</span><span class="sxs-lookup"><span data-stu-id="c65f9-177">N/A</span></span>           | <span data-ttu-id="c65f9-178">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="c65f9-178">D3DVECTOR</span></span> | <span data-ttu-id="c65f9-179">Vecteur de direction de la position du vertex à la position de la lumière.</span><span class="sxs-lookup"><span data-stu-id="c65f9-179">Direction vector from vertex position to the light position.</span></span> |



 

<span data-ttu-id="c65f9-180">La détermination du vecteur à mi-chemin de cette manière peut nécessiter de nombreuses ressources de calcul.</span><span class="sxs-lookup"><span data-stu-id="c65f9-180">Determining the halfway vector in this manner can be computationally intensive.</span></span> <span data-ttu-id="c65f9-181">En guise d’alternative, la définition de D3DRS \_ LOCALVIEWER = **false** indique au système d’agir comme si le point de vue est distant de façon infinie sur l’axe z.</span><span class="sxs-lookup"><span data-stu-id="c65f9-181">As an alternative, setting D3DRS\_LOCALVIEWER = **FALSE** instructs the system to act as though the viewpoint is infinitely distant on the z-axis.</span></span> <span data-ttu-id="c65f9-182">Cela se reflète dans la formule suivante.</span><span class="sxs-lookup"><span data-stu-id="c65f9-182">This is reflected in the following formula.</span></span>

<span data-ttu-id="c65f9-183">**H = normal ((0, 0, 1) + L <sub>répertoire</sub>)**</span><span class="sxs-lookup"><span data-stu-id="c65f9-183">**H = norm((0,0,1) + L<sub>dir</sub>)**</span></span>



 

<span data-ttu-id="c65f9-184">Ce paramètre est moins gourmand en calculs, mais beaucoup moins précis. il est donc mieux utilisé par les applications qui utilisent la projection orthogonale.</span><span class="sxs-lookup"><span data-stu-id="c65f9-184">This setting is less computationally intensive, but much less accurate, so it is best used by applications that use orthogonal projection.</span></span>

## <a name="example"></a><span data-ttu-id="c65f9-185">Exemple</span><span class="sxs-lookup"><span data-stu-id="c65f9-185">Example</span></span>

<span data-ttu-id="c65f9-186">Dans cet exemple, l’objet est coloré à l’aide de la couleur de la lumière spéculaire et d’une couleur spéculaire.</span><span class="sxs-lookup"><span data-stu-id="c65f9-186">In this example, the object is colored using the scene specular light color and a material specular color.</span></span> <span data-ttu-id="c65f9-187">Le code est illustré ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c65f9-187">The code is shown below.</span></span>


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

light.Specular.r = 1.0f;
light.Specular.g = 1.0f;
light.Specular.b = 1.0f;
light.Specular.a = 1.0f;

light.Range = 1000;
light.Falloff = 0;
light.Attenuation0 = 1;
light.Attenuation1 = 0;
light.Attenuation2 = 0;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );
m_pd3dDevice->SetRenderState( D3DRS_SPECULARENABLE, TRUE );

mtrl.Specular.r = 0.5f;
mtrl.Specular.g = 0.5f;
mtrl.Specular.b = 0.5f;
mtrl.Specular.a = 0.5f;
mtrl.Power = 20;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_SPECULARMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="c65f9-188">D’après l’équation, la couleur résultante pour les vertex d’objet est une combinaison de la couleur de l’élément et de la couleur claire.</span><span class="sxs-lookup"><span data-stu-id="c65f9-188">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="c65f9-189">L’illustration suivante montre la couleur de matériau spéculaire, grise, et la couleur d’éclairage spéculaire, qui est blanche.</span><span class="sxs-lookup"><span data-stu-id="c65f9-189">The following two illustration show the specular material color, which is gray, and the specular light color, which is white.</span></span>

![illustration d’une sphère grise](images/amb1.jpg)![illustration d’une sphère blanche](images/lightwhite.jpg)

<span data-ttu-id="c65f9-192">La surbrillance spéculaire qui en résulte est présentée dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="c65f9-192">The resulting specular highlight is shown in the following illustration.</span></span>

![illustration de la surbrillance spéculaire](images/lights.jpg)

<span data-ttu-id="c65f9-194">La combinaison de la surbrillance spéculaire avec l’éclairage ambiant et diffus produit l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="c65f9-194">Combining the specular highlight with the ambient and diffuse lighting produces the following illustration.</span></span> <span data-ttu-id="c65f9-195">Avec les trois types d’éclairage appliqués, cela ressemble plus clairement à un objet réaliste.</span><span class="sxs-lookup"><span data-stu-id="c65f9-195">With all three types of lighting applied, this more clearly resembles a realistic object.</span></span>

![illustration de la combinaison de la mise en surbrillance spéculaire, de l’éclairage ambiant et de l’éclairage diffus](images/lightads.jpg)

<span data-ttu-id="c65f9-197">L’éclairage spéculaire est plus gourmand en calcul que l’éclairage diffus.</span><span class="sxs-lookup"><span data-stu-id="c65f9-197">Specular lighting is more intensive to calculate than diffuse lighting.</span></span> <span data-ttu-id="c65f9-198">Il est généralement utilisé pour fournir des indices visuels sur le matériau en surface.</span><span class="sxs-lookup"><span data-stu-id="c65f9-198">It is typically used to provide visual clues about the surface material.</span></span> <span data-ttu-id="c65f9-199">La mise en surbrillance spéculaire varie en fonction de la taille et de la couleur.</span><span class="sxs-lookup"><span data-stu-id="c65f9-199">The specular highlight varies in size and color with the material of the surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c65f9-200">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c65f9-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c65f9-201">Mathématiques d’éclairage</span><span class="sxs-lookup"><span data-stu-id="c65f9-201">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



