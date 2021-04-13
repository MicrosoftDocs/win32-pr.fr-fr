---
description: Les matériaux décrivent comment les polygones reflètent la lumière ou apparaissent pour émettre de la lumière dans une scène 3D.
ms.assetid: vs|directx_sdk|~\materials.htm
title: Matériaux (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e75953fd5839e1b3e7b9cc89b7331147cdb585
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104559675"
---
# <a name="materials-direct3d-9"></a><span data-ttu-id="f902d-103">Matériaux (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f902d-103">Materials (Direct3D 9)</span></span>

<span data-ttu-id="f902d-104">Les matériaux décrivent comment les polygones reflètent la lumière ou apparaissent pour émettre de la lumière dans une scène 3D.</span><span class="sxs-lookup"><span data-stu-id="f902d-104">Materials describe how polygons reflect light or appear to emit light in a 3D scene.</span></span> <span data-ttu-id="f902d-105">Les propriétés de matériau détaillent la réflexion diffuse d’un matériau, la réflexion ambiante, les émissions légères et les caractéristiques de surbrillance spéculaire.</span><span class="sxs-lookup"><span data-stu-id="f902d-105">Material properties detail a material's diffuse reflection, ambient reflection, light emission, and specular highlight characteristics.</span></span> <span data-ttu-id="f902d-106">Direct3D utilise la structure [**D3DMATERIAL9**](d3dmaterial9.md) pour transporter toutes les informations de propriété de matériau.</span><span class="sxs-lookup"><span data-stu-id="f902d-106">Direct3D uses the [**D3DMATERIAL9**](d3dmaterial9.md) structure to carry all material property information.</span></span> <span data-ttu-id="f902d-107">À l’exception de la propriété spéculaire, chaque propriété est décrite comme une couleur RVBA qui représente la proportion des parties rouge, verte et bleue d’un type de lumière donné qu’elle reflète et un facteur de fusion alpha.</span><span class="sxs-lookup"><span data-stu-id="f902d-107">With the exception of the specular property, each property is described as an RGBA color that represents how much of the red, green, and blue parts of a given type of light it reflects, and an alpha blending factor.</span></span>

## <a name="diffuse-and-ambient-reflection"></a><span data-ttu-id="f902d-108">Réflexion diffuse et ambiante</span><span class="sxs-lookup"><span data-stu-id="f902d-108">Diffuse and Ambient Reflection</span></span>

<span data-ttu-id="f902d-109">Les membres diffus et ambiant de la structure [**D3DMATERIAL9**](d3dmaterial9.md) décrivent comment un matériau reflète la lumière ambiante et diffuse dans une scène.</span><span class="sxs-lookup"><span data-stu-id="f902d-109">The Diffuse and Ambient members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure describe how a material reflects the ambient and diffuse light in a scene.</span></span> <span data-ttu-id="f902d-110">Étant donné que la plupart des scènes contiennent bien plus de lumière diffuse que la lumière ambiante, la réflexion diffuse joue la plus grande partie de la détermination de la couleur.</span><span class="sxs-lookup"><span data-stu-id="f902d-110">Because most scenes contain much more diffuse light than ambient light, diffuse reflection plays the largest part in determining color.</span></span> <span data-ttu-id="f902d-111">En outre, étant donné que la lumière diffuse est directionnelle, l’angle d’incidence pour la lumière diffuse affecte l’intensité globale de la réflexion.</span><span class="sxs-lookup"><span data-stu-id="f902d-111">Additionally, because diffuse light is directional, the angle of incidence for diffuse light affects the overall intensity of the reflection.</span></span> <span data-ttu-id="f902d-112">La réflexion diffuse est la plus grande lorsque la lumière fait apparaître un sommet parallèlement à la normale du vertex.</span><span class="sxs-lookup"><span data-stu-id="f902d-112">Diffuse reflection is greatest when the light strikes a vertex parallel to the vertex normal.</span></span> <span data-ttu-id="f902d-113">À mesure que l’angle augmente, l’effet de la réflexion diffuse diminue.</span><span class="sxs-lookup"><span data-stu-id="f902d-113">As the angle increases, the effect of diffuse reflection diminishes.</span></span> <span data-ttu-id="f902d-114">La quantité de lumière réfléchie est le cosinus de l’angle entre la lumière entrante et le vertex normal, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="f902d-114">The amount of light reflected is the cosine of the angle between the incoming light and the vertex normal, as shown in the following illustration.</span></span>

![illustration de la quantité de lumière réfléchie](images/incident.png)

<span data-ttu-id="f902d-116">La réflexion ambiante, comme la lumière ambiante, est non directionnelle.</span><span class="sxs-lookup"><span data-stu-id="f902d-116">Ambient reflection, like ambient light, is nondirectional.</span></span> <span data-ttu-id="f902d-117">La réflexion ambiante a un impact moindre sur la couleur apparente d’un objet rendu, mais elle affecte la couleur globale et est plus perceptible lorsque la lumière diffuse est minime ou non.</span><span class="sxs-lookup"><span data-stu-id="f902d-117">Ambient reflection has a lesser impact on the apparent color of a rendered object, but it does affect the overall color and is most noticeable when little or no diffuse light reflects off the material.</span></span> <span data-ttu-id="f902d-118">La réflexion ambiante d’un matériau est affectée par la lumière ambiante définie pour une scène en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) avec l' \_ indicateur ambiant D3DRS.</span><span class="sxs-lookup"><span data-stu-id="f902d-118">A material's ambient reflection is affected by the ambient light set for a scene by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method with the D3DRS\_AMBIENT flag.</span></span>

<span data-ttu-id="f902d-119">La réflexion diffuse et ambiante fonctionne ensemble pour déterminer la couleur perçue d’un objet et sont généralement des valeurs identiques.</span><span class="sxs-lookup"><span data-stu-id="f902d-119">Diffuse and ambient reflection work together to determine the perceived color of an object, and are usually identical values.</span></span> <span data-ttu-id="f902d-120">Par exemple, pour restituer un objet cristallin bleu, vous créez un matériau qui reflète uniquement le composant bleu de diffusion et de lumière ambiante.</span><span class="sxs-lookup"><span data-stu-id="f902d-120">For example, to render a blue crystalline object, you create a material that reflects only the blue component of diffuse and ambient light.</span></span> <span data-ttu-id="f902d-121">Lorsqu’il est placé dans une pièce avec une lumière blanche, le cristal semble être bleu.</span><span class="sxs-lookup"><span data-stu-id="f902d-121">When placed in a room with a white light, the crystal appears to be blue.</span></span> <span data-ttu-id="f902d-122">Toutefois, dans une salle qui a uniquement une lumière rouge, le même cristal semble être noir, car son matériau ne reflète pas la lumière rouge.</span><span class="sxs-lookup"><span data-stu-id="f902d-122">However, in a room that has only red light, the same crystal would appear to be black, because its material doesn't reflect red light.</span></span>

## <a name="emission"></a><span data-ttu-id="f902d-123">Émission</span><span class="sxs-lookup"><span data-stu-id="f902d-123">Emission</span></span>

<span data-ttu-id="f902d-124">Les matériaux peuvent être utilisés pour qu’un objet rendu semble être auto-lumineux.</span><span class="sxs-lookup"><span data-stu-id="f902d-124">Materials can be used to make a rendered object appear to be self-luminous.</span></span> <span data-ttu-id="f902d-125">Le membre émissif de la structure [**D3DMATERIAL9**](d3dmaterial9.md) est utilisé pour décrire la couleur et la transparence de la lumière émise.</span><span class="sxs-lookup"><span data-stu-id="f902d-125">The Emissive member of the [**D3DMATERIAL9**](d3dmaterial9.md) structure is used to describe the color and transparency of the emitted light.</span></span> <span data-ttu-id="f902d-126">L’émission affecte la couleur d’un objet et peut, par exemple, rendre un matériau sombre plus clair et prendre en partie la couleur émise.</span><span class="sxs-lookup"><span data-stu-id="f902d-126">Emission affects an object's color and can, for example, make a dark material brighter and take on part of the emitted color.</span></span>

<span data-ttu-id="f902d-127">Vous pouvez utiliser la propriété émissif d’un matériau pour ajouter l’illusion qu’un objet émet de la lumière, sans impliquer la surcharge de calcul de l’ajout d’une lumière à la scène.</span><span class="sxs-lookup"><span data-stu-id="f902d-127">You can use a material's emissive property to add the illusion that an object is emitting light, without incurring the computational overhead of adding a light to the scene.</span></span> <span data-ttu-id="f902d-128">Dans le cas du cristal bleu, la propriété émissif est utile si vous souhaitez que le cristal semble allumé, mais pas pour les autres objets de la scène.</span><span class="sxs-lookup"><span data-stu-id="f902d-128">In the case of the blue crystal, the emissive property is useful if you want to make the crystal appear to light up, but not cast light on other objects in the scene.</span></span> <span data-ttu-id="f902d-129">N’oubliez pas que les matériaux avec des propriétés émissif n’émettent pas de lumière qui peuvent être reflétées par d’autres objets dans une scène.</span><span class="sxs-lookup"><span data-stu-id="f902d-129">Remember, materials with emissive properties don't emit light that can be reflected by other objects in a scene.</span></span> <span data-ttu-id="f902d-130">Pour obtenir cette lumière réfléchie, vous devez placer une lumière supplémentaire dans la scène.</span><span class="sxs-lookup"><span data-stu-id="f902d-130">To achieve this reflected light, you need to place an additional light within the scene.</span></span>

## <a name="specular-reflection"></a><span data-ttu-id="f902d-131">Réflexion spéculaire</span><span class="sxs-lookup"><span data-stu-id="f902d-131">Specular Reflection</span></span>

<span data-ttu-id="f902d-132">La réflexion spéculaire crée des surbrillances sur les objets, ce qui les rend brillants.</span><span class="sxs-lookup"><span data-stu-id="f902d-132">Specular reflection creates highlights on objects, making them appear shiny.</span></span> <span data-ttu-id="f902d-133">La structure [**D3DMATERIAL9**](d3dmaterial9.md) contient deux membres qui décrivent la couleur de surbrillance spéculaire ainsi que la brillance globale du matériau.</span><span class="sxs-lookup"><span data-stu-id="f902d-133">The [**D3DMATERIAL9**](d3dmaterial9.md) structure contains two members that describe the specular highlight color as well as the material's overall shininess.</span></span> <span data-ttu-id="f902d-134">Vous établissez la couleur des surbrillances spéculaires en définissant le membre spéculaire sur la couleur RVBA souhaitée. les couleurs les plus courantes sont blanches ou gris clair.</span><span class="sxs-lookup"><span data-stu-id="f902d-134">You establish the color of the specular highlights by setting the Specular member to the desired RGBA color - the most common colors are white or light gray.</span></span> <span data-ttu-id="f902d-135">Les valeurs que vous définissez dans le contrôle des membres d’alimentation déterminent la netteté des effets spéculaires.</span><span class="sxs-lookup"><span data-stu-id="f902d-135">The values you set in the Power member control how sharp the specular effects are.</span></span>

<span data-ttu-id="f902d-136">Les surbrillances spéculaires peuvent créer des effets spectaculaires.</span><span class="sxs-lookup"><span data-stu-id="f902d-136">Specular highlights can create dramatic effects.</span></span> <span data-ttu-id="f902d-137">Dessin à nouveau sur l’analogie monocristal bleue : une valeur de puissance plus grande crée des surbrillances spéculaires plus nettes, ce qui rend le cristal très brillant.</span><span class="sxs-lookup"><span data-stu-id="f902d-137">Drawing again on the blue crystal analogy: a larger Power value creates sharper specular highlights, making the crystal appear to be quite shiny.</span></span> <span data-ttu-id="f902d-138">Des valeurs plus petites augmentent la zone de l’effet, créant une réflexion terne qui rend l’apparence cristalline.</span><span class="sxs-lookup"><span data-stu-id="f902d-138">Smaller values increase the area of the effect, creating a dull reflection that make the crystal look frosty.</span></span> <span data-ttu-id="f902d-139">Pour rendre un objet véritablement mat, définissez le membre d’alimentation sur zéro et la couleur de l’éclairage spéculaire sur noir.</span><span class="sxs-lookup"><span data-stu-id="f902d-139">To make an object truly matte, set the Power member to zero and the color in Specular to black.</span></span> <span data-ttu-id="f902d-140">Faites des essais avec différents niveaux de réflexion pour produire une apparence réaliste pour vos besoins.</span><span class="sxs-lookup"><span data-stu-id="f902d-140">Experiment with different levels of reflection to produce a realistic appearance for your needs.</span></span> <span data-ttu-id="f902d-141">L’illustration suivante montre deux modèles identiques.</span><span class="sxs-lookup"><span data-stu-id="f902d-141">The following illustration shows two identical models.</span></span> <span data-ttu-id="f902d-142">Celui de gauche utilise une puissance de réflexion spéculaire de 10 ; le modèle de droite n’a pas de réflexion spéculaire.</span><span class="sxs-lookup"><span data-stu-id="f902d-142">The one on the left uses a specular reflection power of 10; the model on the right has no specular reflection.</span></span>

![illustration des modèles de réflexion spéculaire](images/spechigh.png)

## <a name="setting-material-properties"></a><span data-ttu-id="f902d-144">Définition des propriétés d’un matériau</span><span class="sxs-lookup"><span data-stu-id="f902d-144">Setting Material Properties</span></span>

<span data-ttu-id="f902d-145">Les appareils de rendu Direct3D peuvent effectuer un rendu avec un ensemble de propriétés de matériau à la fois.</span><span class="sxs-lookup"><span data-stu-id="f902d-145">Direct3D rendering devices can render with one set of material properties at a time.</span></span>

<span data-ttu-id="f902d-146">Dans une application C++, vous définissez les propriétés de matériau que le système utilise en préparant une structure [**D3DMATERIAL9**](d3dmaterial9.md) , puis en appelant la méthode [**IDirect3DDevice9 :: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) .</span><span class="sxs-lookup"><span data-stu-id="f902d-146">In a C++ application, you set the material properties that the system uses by preparing a [**D3DMATERIAL9**](d3dmaterial9.md) structure, and then calling the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method.</span></span>

<span data-ttu-id="f902d-147">Pour préparer l’utilisation de la structure [**D3DMATERIAL9**](d3dmaterial9.md) , définissez les informations de propriété dans la structure pour créer l’effet souhaité pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="f902d-147">To prepare the [**D3DMATERIAL9**](d3dmaterial9.md) structure for use, set the property information in the structure to create the desired effect during rendering.</span></span> <span data-ttu-id="f902d-148">L’exemple de code suivant configure la structure **D3DMATERIAL9** pour un matériau violet avec des surbrillances spéculaires blanches nettes.</span><span class="sxs-lookup"><span data-stu-id="f902d-148">The following code example sets up the **D3DMATERIAL9** structure for a purple material with sharp white specular highlights.</span></span>


```
D3DMATERIAL9 mat;

// Set the RGBA for diffuse reflection.
mat.Diffuse.r = 0.5f;
mat.Diffuse.g = 0.0f;
mat.Diffuse.b = 0.5f;
mat.Diffuse.a = 1.0f;

// Set the RGBA for ambient reflection.
mat.Ambient.r = 0.5f;
mat.Ambient.g = 0.0f;
mat.Ambient.b = 0.5f;
mat.Ambient.a = 1.0f;

// Set the color and sharpness of specular highlights.
mat.Specular.r = 1.0f;
mat.Specular.g = 1.0f;
mat.Specular.b = 1.0f;
mat.Specular.a = 1.0f;
mat.Power = 50.0f;

// Set the RGBA for emissive color.
mat.Emissive.r = 0.0f;
mat.Emissive.g = 0.0f;
mat.Emissive.b = 0.0f;
mat.Emissive.a = 0.0f;
```



<span data-ttu-id="f902d-149">Après la préparation de la structure [**D3DMATERIAL9**](d3dmaterial9.md) , vous appliquez les propriétés en appelant la méthode [**IDirect3DDevice9 :: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) du périphérique de rendu.</span><span class="sxs-lookup"><span data-stu-id="f902d-149">After preparing the [**D3DMATERIAL9**](d3dmaterial9.md) structure, you apply the properties by calling the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method of the rendering device.</span></span> <span data-ttu-id="f902d-150">Cette méthode accepte l’adresse d’une structure **D3DMATERIAL9** préparée comme son seul paramètre.</span><span class="sxs-lookup"><span data-stu-id="f902d-150">This method accepts the address of a prepared **D3DMATERIAL9** structure as its only parameter.</span></span> <span data-ttu-id="f902d-151">Vous pouvez appeler **IDirect3DDevice9 :: SetMaterial** avec de nouvelles informations en fonction des besoins pour mettre à jour les propriétés de matériau de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f902d-151">You can call **IDirect3DDevice9::SetMaterial** with new information as needed to update the material properties for the device.</span></span> <span data-ttu-id="f902d-152">L’exemple de code suivant montre comment cela peut s’afficher dans le code.</span><span class="sxs-lookup"><span data-stu-id="f902d-152">The following code example shows how this might look in code.</span></span>


```
// This code example uses the material properties defined for 
// the mat variable earlier in this topic. The pd3dDev is assumed
// to be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
hr = pd3dDev->SetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



<span data-ttu-id="f902d-153">Lorsque vous créez un appareil Direct3D, le matériel actuel est automatiquement défini sur la valeur par défaut indiquée dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f902d-153">When you create a Direct3D device, the current material is automatically set to the default shown in the following table.</span></span>



| <span data-ttu-id="f902d-154">Membre</span><span class="sxs-lookup"><span data-stu-id="f902d-154">Member</span></span>   | <span data-ttu-id="f902d-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="f902d-155">Value</span></span>                |
|----------|----------------------|
| <span data-ttu-id="f902d-156">Diffus</span><span class="sxs-lookup"><span data-stu-id="f902d-156">Diffuse</span></span>  | <span data-ttu-id="f902d-157">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="f902d-157">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="f902d-158">Spéculaire</span><span class="sxs-lookup"><span data-stu-id="f902d-158">Specular</span></span> | <span data-ttu-id="f902d-159">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="f902d-159">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="f902d-160">Ambiant</span><span class="sxs-lookup"><span data-stu-id="f902d-160">Ambient</span></span>  | <span data-ttu-id="f902d-161">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="f902d-161">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="f902d-162">Émissif</span><span class="sxs-lookup"><span data-stu-id="f902d-162">Emissive</span></span> | <span data-ttu-id="f902d-163">(R:0, G:0, B:0, A:0)</span><span class="sxs-lookup"><span data-stu-id="f902d-163">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="f902d-164">Power</span><span class="sxs-lookup"><span data-stu-id="f902d-164">Power</span></span>    | <span data-ttu-id="f902d-165">(0,0)</span><span class="sxs-lookup"><span data-stu-id="f902d-165">(0.0)</span></span>                |



 

## <a name="retrieving-material-properties"></a><span data-ttu-id="f902d-166">Récupération des propriétés de matériel</span><span class="sxs-lookup"><span data-stu-id="f902d-166">Retrieving Material Properties</span></span>

<span data-ttu-id="f902d-167">Vous récupérez les propriétés de matériau que l’appareil de rendu utilise actuellement en appelant la méthode [**IDirect3DDevice9 :: GetMaterial**](/windows/desktop/api) pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f902d-167">You retrieve the material properties that the rendering device is currently using by calling the [**IDirect3DDevice9::GetMaterial**](/windows/desktop/api) method for the device.</span></span> <span data-ttu-id="f902d-168">Contrairement à la méthode [**IDirect3DDevice9 :: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) , **IDirect3DDevice9 :: GetMaterial** ne requiert pas de préparation.</span><span class="sxs-lookup"><span data-stu-id="f902d-168">Unlike the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method, **IDirect3DDevice9::GetMaterial** doesn't require preparation.</span></span> <span data-ttu-id="f902d-169">La méthode **IDirect3DDevice9 :: GetMaterial** accepte l’adresse d’une structure [**D3DMATERIAL9**](d3dmaterial9.md) et remplit la structure fournie avec les informations qui décrivent les propriétés de matière actuelles avant de retourner.</span><span class="sxs-lookup"><span data-stu-id="f902d-169">The **IDirect3DDevice9::GetMaterial** method accepts the address of a [**D3DMATERIAL9**](d3dmaterial9.md) structure, and fills the provided structure with information describing the current material properties before returning.</span></span>


```
// For this example, the pd3dDev variable is assumed to 
// be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
D3DMATERIAL9 mat;

hr = pd3dDev->GetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



> [!Note]  
> <span data-ttu-id="f902d-170">Si votre application ne spécifie pas de propriétés de matériau pour le rendu, le système utilise un matériau par défaut.</span><span class="sxs-lookup"><span data-stu-id="f902d-170">If your application does not specify material properties for rendering, the system uses a default material.</span></span> <span data-ttu-id="f902d-171">La matière par défaut reflète tout le clair diffus, par exemple, sans réflexion ambiante ou spéculaire, et sans couleur émissif.</span><span class="sxs-lookup"><span data-stu-id="f902d-171">The default material reflects all diffuse light - white, for example - with no ambient or specular reflection, and no emissive color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f902d-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f902d-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f902d-173">Lumières et matériaux</span><span class="sxs-lookup"><span data-stu-id="f902d-173">Lights and Materials</span></span>](lights-and-materials.md)
</dt> </dl>

 

 
