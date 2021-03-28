---
title: Plans de clip utilisateur sur le matériel de niveau de fonctionnalité 9
description: À compter de Windows 8, le langage HLSL (High Level Shader Language) de Microsoft prend en charge une syntaxe que vous pouvez utiliser avec l’API Microsoft Direct3D 11 pour spécifier des plans de clip utilisateur sur le niveau de fonctionnalité 9 \_ x et plus.
ms.assetid: C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968831ca39f2501a44b00f202fd8dfda1f92d1e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315570"
---
# <a name="user-clip-planes-on-feature-level-9-hardware"></a><span data-ttu-id="541e7-103">Plans de clip utilisateur sur le matériel de niveau de fonctionnalité 9</span><span class="sxs-lookup"><span data-stu-id="541e7-103">User clip planes on feature level 9 hardware</span></span>

<span data-ttu-id="541e7-104">À compter de Windows 8, le langage HLSL (High Level Shader Language) de Microsoft prend en charge une syntaxe que vous pouvez utiliser avec l’API Microsoft Direct3D 11 pour spécifier des plans de clip utilisateur sur le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x et plus.</span><span class="sxs-lookup"><span data-stu-id="541e7-104">Starting with Windows 8, Microsoft High Level Shader Language (HLSL) supports a syntax that you can use with the Microsoft Direct3D 11 API to specify user clip planes on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="541e7-105">Vous pouvez utiliser cette syntaxe pour écrire un nuanceur, puis utiliser cet objet de nuanceur avec l’API Direct3D 11 pour exécuter tous les niveaux de fonctionnalité Direct3D.</span><span class="sxs-lookup"><span data-stu-id="541e7-105">You can use this clip-planes syntax to write a shader, and then use that shader object with the Direct3D 11 API to run on all Direct3D feature levels.</span></span>

-   [<span data-ttu-id="541e7-106">Contexte</span><span class="sxs-lookup"><span data-stu-id="541e7-106">Background</span></span>](#background-reading)
-   [<span data-ttu-id="541e7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="541e7-107">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="541e7-108">Création de plans de clip dans l’espace sur le niveau de fonctionnalité 9 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="541e7-108">Creating clip planes in clip space on feature level 9 and higher</span></span>](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [<span data-ttu-id="541e7-109">Lecture en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="541e7-109">Background reading</span></span>](#background-reading)
    -   [<span data-ttu-id="541e7-110">niveaux de fonctionnalité de 10Level9</span><span class="sxs-lookup"><span data-stu-id="541e7-110">10Level9 feature levels</span></span>](#10level9-feature-levels)
    -   [<span data-ttu-id="541e7-111">Math plan de coupe</span><span class="sxs-lookup"><span data-stu-id="541e7-111">Clip plane math</span></span>](#clip-plane-math)
    -   [<span data-ttu-id="541e7-112">Découpage dans l’espace d’affichage</span><span class="sxs-lookup"><span data-stu-id="541e7-112">Clipping in view space</span></span>](#clipping-in-view-space)
    -   [<span data-ttu-id="541e7-113">Matrice de projection</span><span class="sxs-lookup"><span data-stu-id="541e7-113">Projection matrix</span></span>](#projection-matrix)
    -   [<span data-ttu-id="541e7-114">Plan de découpage de l’espace</span><span class="sxs-lookup"><span data-stu-id="541e7-114">Clip space clip plane</span></span>](#clip-space-clip-plane)
-   [<span data-ttu-id="541e7-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="541e7-115">Related topics</span></span>](#related-topics)

## <a name="background"></a><span data-ttu-id="541e7-116">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="541e7-116">Background</span></span>

<span data-ttu-id="541e7-117">Vous pouvez accéder aux plans de clips utilisateur dans l’API Microsoft Direct3D 9 via les méthodes [**IDirect3DDevice9 :: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) et [**IDirect3DDevice9 :: GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) .</span><span class="sxs-lookup"><span data-stu-id="541e7-117">You can access user clip planes in the Microsoft Direct3D 9 API via [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) and [**IDirect3DDevice9::GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) methods.</span></span> <span data-ttu-id="541e7-118">Dans Microsoft Direct3D 10 et versions ultérieures, vous pouvez accéder aux plans d’utilisateur à l’aide de la sémantique [SV \_ ClipDistance](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="541e7-118">In Microsoft Direct3D 10 and later, you can access user clip planes through the [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="541e7-119">Mais avant Windows 8, SV \_ ClipDistance n’était pas disponible [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) pour \_ le matériel de niveau de fonctionnalité 9 x dans les API Direct3D 10 ou Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="541e7-119">But before Windows 8, SV\_ClipDistance was not available for [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x hardware in the Direct3D 10 or Direct3D 11 APIs.</span></span> <span data-ttu-id="541e7-120">Donc, avant Windows 8, le seul moyen d’accéder aux plans de l’utilisateur avec le matériel de niveau de fonctionnalité 9 \_ x consistait à utiliser l’API Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="541e7-120">So, before Windows 8, the only way to access user clip planes with feature level 9\_x hardware was through the Direct3D 9 API.</span></span> <span data-ttu-id="541e7-121">Les applications Direct3D du Windows Store ne peuvent pas utiliser l’API Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="541e7-121">Direct3D Windows Store apps can't use the Direct3D 9 API.</span></span> <span data-ttu-id="541e7-122">Ici, nous décrivons la syntaxe que vous pouvez utiliser pour accéder aux plans de l’utilisateur via l’API Direct3D 11 au niveau de la fonctionnalité 9 \_ x et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="541e7-122">Here we describe the syntax that you can use to access user clip planes through the Direct3D 11 API on feature level 9\_x and higher.</span></span>

<span data-ttu-id="541e7-123">Les applications utilisent des plans de coupe pour définir un ensemble de plans invisibles dans le monde 3D qui découpent (éliminent) toutes les primitives dessinées.</span><span class="sxs-lookup"><span data-stu-id="541e7-123">Apps use clip planes to define a set of invisible planes within the 3D world that clip (throw away) all drawn primitives.</span></span> <span data-ttu-id="541e7-124">Windows ne dessinera aucun pixel qui se trouve du côté négatif des plans de coupe.</span><span class="sxs-lookup"><span data-stu-id="541e7-124">Windows won't draw any pixel that is on the negative side of any clip planes.</span></span> <span data-ttu-id="541e7-125">Les applications peuvent ensuite utiliser des plans de clip pour restituer les réflexions planaires.</span><span class="sxs-lookup"><span data-stu-id="541e7-125">Apps can then use clip planes to render planar reflections.</span></span>

## <a name="syntax"></a><span data-ttu-id="541e7-126">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="541e7-126">Syntax</span></span>

<span data-ttu-id="541e7-127">Utilisez cette syntaxe pour déclarer des plans d’éléments en tant qu’attributs de fonction dans une [déclaration de fonction](dx-graphics-hlsl-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="541e7-127">Use this syntax to declare clip planes as function attributes in a [function declaration](dx-graphics-hlsl-function-syntax.md).</span></span> <span data-ttu-id="541e7-128">Par exemple, nous utilisons ici la syntaxe sur un fragment de nuanceur de sommets :</span><span class="sxs-lookup"><span data-stu-id="541e7-128">For example, here we use the syntax on a vertex shader fragment:</span></span>

``` syntax
cbuffer ClipPlaneConstantBuffer 
{
       float4 clipPlane1;
       float4 clipPlane2;
};

[clipplanes(clipPlane1,clipPlane2)]
VertexShaderOutput main(VertexShaderInput input)
{
       // the rest of the vertex shader doesn't refer to the clip plane
 
       …
 
       return output;
}
```

<span data-ttu-id="541e7-129">Cet exemple pour un fragment de nuanceur de sommets désigne deux plans de clip.</span><span class="sxs-lookup"><span data-stu-id="541e7-129">This example for a vertex shader fragment denotes two clip planes.</span></span> <span data-ttu-id="541e7-130">Il montre que vous devez placer le nouvel attribut **clipplanes** entre crochets immédiatement avant la valeur de retour du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="541e7-130">It shows that you need to place the new **clipplanes** attribute within square brackets immediately before the return value of the vertex shader.</span></span> <span data-ttu-id="541e7-131">Entre parenthèses après l’attribut **clipplanes** , vous fournissez une liste de 6 constantes **float4** au maximum qui définissent les coefficients de plan pour chaque plan de découpage actif.</span><span class="sxs-lookup"><span data-stu-id="541e7-131">Within parentheses after the **clipplanes** attribute, you provide a list of up to 6 **float4** constants that define the plane coefficients for each active clip plane.</span></span> <span data-ttu-id="541e7-132">L’exemple montre également que vous devez faire en sorte que les coefficients de chaque plan résident dans une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="541e7-132">The example also shows that you need to make the coefficients of each plane reside in a constant buffer.</span></span>

> [!Note]  
> <span data-ttu-id="541e7-133">Aucune syntaxe n’est disponible pour désactiver dynamiquement un plan de découpage.</span><span class="sxs-lookup"><span data-stu-id="541e7-133">There is no syntax available to disable a clip plane dynamically.</span></span> <span data-ttu-id="541e7-134">Vous devez recompiler un nuanceur identique qui ne possède pas d’attribut **clipplanes** , ou votre application peut définir les coefficients dans votre mémoire tampon constante à zéro afin que le plan n’affecte plus aucune géométrie.</span><span class="sxs-lookup"><span data-stu-id="541e7-134">You must either recompile an otherwise identical shader with no **clipplanes** attribute, or your app can set the coefficients in your constant buffer to zero so that the plane no longer affects any geometry.</span></span>

 

<span data-ttu-id="541e7-135">Cette syntaxe est disponible pour n’importe quelle cible de nuanceur de sommets 4,0 ou ultérieur, qui comprend vs \_ 4 \_ 0 \_ niveau \_ 9 \_ 1 et vs \_ 4 \_ 0 \_ niveau \_ 9 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="541e7-135">This syntax is available for any 4.0 or later vertex shader target, which includes vs\_4\_0\_level\_9\_1 and vs\_4\_0\_level\_9\_3.</span></span>

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a><span data-ttu-id="541e7-136">Création de plans de clip dans l’espace sur le niveau de fonctionnalité 9 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="541e7-136">Creating clip planes in clip space on feature level 9 and higher</span></span>

<span data-ttu-id="541e7-137">Ici, nous montrons comment créer des plans de clips dans l’espace sur les [fonctionnalités](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x et supérieures.</span><span class="sxs-lookup"><span data-stu-id="541e7-137">Here we show how to create clip planes in clip space on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

### <a name="background-reading"></a><span data-ttu-id="541e7-138">Lecture en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="541e7-138">Background reading</span></span>

<span data-ttu-id="541e7-139">« Introduction à la programmation de jeux en 3D avec DirectX 10 » de Frank D. Luna explique l’arrière-plan mathématique des graphiques (chapitres 1, 2 et 3) dont vous avez besoin, ainsi que les différentes transformations d’espaces et d’espaces qui se produisent dans le nuanceur de sommets (sections 5,6 et 5,8).</span><span class="sxs-lookup"><span data-stu-id="541e7-139">"Introduction to 3D Game Programming with DirectX 10" by Frank D. Luna explains the graphics math background (chapters 1, 2 and 3) you need, and the various spaces and space transformations that occur in the vertex shader (sections 5.6 and 5.8).</span></span>

### <a name="10level9-feature-levels"></a><span data-ttu-id="541e7-140">niveaux de fonctionnalité de 10Level9</span><span class="sxs-lookup"><span data-stu-id="541e7-140">10Level9 feature levels</span></span>

<span data-ttu-id="541e7-141">Dans Direct3D 10 et versions ultérieures, vous pouvez découper n’importe quel espace logique, souvent dans l’espace universel ou dans l’espace d’affichage.</span><span class="sxs-lookup"><span data-stu-id="541e7-141">In Direct3D 10 and later, you can clip in any space that makes sense, often in world space or view space.</span></span> <span data-ttu-id="541e7-142">Mais Direct3D 9 utilise l’espace de clip, qui est un espace de projection de préversion préalable.</span><span class="sxs-lookup"><span data-stu-id="541e7-142">But Direct3D 9 uses clip space, which is pre perspective divide projection space.</span></span> <span data-ttu-id="541e7-143">Les vecteurs sont dans l’espace de l’élément lorsque le nuanceur de sommets les passe aux étapes qui suivent dans le [pipeline Graphics](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).</span><span class="sxs-lookup"><span data-stu-id="541e7-143">Vectors are in clip space when the vertex shader passes them to stages that follow in the [graphics pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).</span></span>

<span data-ttu-id="541e7-144">Lorsque vous écrivez une application du Windows Store, vous devez utiliser les niveaux de fonctionnalité 10Level9 ([niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x) pour que l’application puisse s’exécuter sur du matériel de niveau de fonctionnalité 9 \_ x et supérieur.</span><span class="sxs-lookup"><span data-stu-id="541e7-144">When you write a Windows Store app, you must use 10Level9 feature levels ([feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x) so the app can run on feature level 9\_x and higher hardware.</span></span> <span data-ttu-id="541e7-145">Étant donné que votre application prend en charge le niveau de fonctionnalité 9 \_ x et les versions ultérieures, vous devez également utiliser la fonction d’application commune des plans de clip dans l’espace.</span><span class="sxs-lookup"><span data-stu-id="541e7-145">Because your app supports feature level 9\_x and higher, you must also use the common capability of applying clip planes in clip space.</span></span>

<span data-ttu-id="541e7-146">Quand vous compilez un nuanceur vertex avec vs \_ 4 \_ 0 \_ niveau \_ 9 \_ 1 ou version ultérieure, ce nuanceur vertex peut utiliser l’attribut **clipplanes** .</span><span class="sxs-lookup"><span data-stu-id="541e7-146">When you compile a vertex shader with vs\_4\_0\_level\_9\_1 or later, that vertex shader can use the **clipplanes** attribute.</span></span> <span data-ttu-id="541e7-147">Un objet Direct3D 10 ou version ultérieure possède un produit scalaire du vertex émis qui contient chacune des constantes globales **float4** spécifiées dans l’attribut.</span><span class="sxs-lookup"><span data-stu-id="541e7-147">A Direct3D 10 or later object has a dot product of the emitted vertex that contains each of the **float4** global constants specified in the attribute.</span></span> <span data-ttu-id="541e7-148">L’objet Direct3D 9 a suffisamment de métadonnées pour obliger le runtime 10Level9 à émettre les appels appropriés à [**IDirect3DDevice9 :: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).</span><span class="sxs-lookup"><span data-stu-id="541e7-148">The Direct3D 9 object has enough meta data to cause the 10Level9 runtime to issue the appropriate calls to [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).</span></span>

### <a name="clip-plane-math"></a><span data-ttu-id="541e7-149">Math plan de coupe</span><span class="sxs-lookup"><span data-stu-id="541e7-149">Clip plane math</span></span>

<span data-ttu-id="541e7-150">Un plan de découpage est défini par un vecteur avec 4 composants.</span><span class="sxs-lookup"><span data-stu-id="541e7-150">A clip plane is defined by a vector with 4 components.</span></span> <span data-ttu-id="541e7-151">Les trois premiers composants définissent un vecteur x, y, z qui émane de l’origine de l’espace que vous souhaitez découper.</span><span class="sxs-lookup"><span data-stu-id="541e7-151">The first three components define an x, y, z vector that emanates from the origin in the space we want to clip.</span></span> <span data-ttu-id="541e7-152">Ce vecteur implique un plan, perpendiculaire au vecteur et s’exécutant par le biais de l’origine.</span><span class="sxs-lookup"><span data-stu-id="541e7-152">This vector implies a plane, perpendicular to the vector and running through the origin.</span></span> <span data-ttu-id="541e7-153">Windows conserve tous les pixels du côté vecteur du plan et découpe tous les pixels situés derrière le plan.</span><span class="sxs-lookup"><span data-stu-id="541e7-153">Windows keeps all pixels on the vector side of the plane and clips all pixels behind the plane.</span></span> <span data-ttu-id="541e7-154">Le composant w est repousse le plan vers l’arrière et entraîne une réduction de la valeur de Windows (une w négative entraîne le découpage de Windows) le long de la ligne vectorielle.</span><span class="sxs-lookup"><span data-stu-id="541e7-154">The forth w component pushes the plane back and causes Windows to clip less (a negative w causes Windows to clip more) along the vector line.</span></span> <span data-ttu-id="541e7-155">Si les composants x, y, z composent un vecteur unitaire (normalisé), w pousse les unités du plan w vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="541e7-155">If the x, y, z components compose a unit (normalized) vector, w pushes the plane w units back.</span></span>

<span data-ttu-id="541e7-156">La mathématique que l’unité de traitement graphique (GPU) effectue pour déterminer le découpage est un simple point entre le vecteur de vertex (x, y, z, 1) et le vecteur du plan de découpage.</span><span class="sxs-lookup"><span data-stu-id="541e7-156">The math that the graphics processing unit (GPU) performs to determine clipping is a simple dot product between the vertex vector (x, y, z, 1) and the clipping plane vector.</span></span> <span data-ttu-id="541e7-157">Cette opération mathématique crée une longueur de projection sur le vecteur de plan de découpage.</span><span class="sxs-lookup"><span data-stu-id="541e7-157">This math operation creates a projection length on the clip plane vector.</span></span> <span data-ttu-id="541e7-158">Un point négatif indique que le vertex se trouve sur le côté coupé du plan.</span><span class="sxs-lookup"><span data-stu-id="541e7-158">A negative dot product shows the vertex to be on the clipped side of the plane.</span></span>

### <a name="clipping-in-view-space"></a><span data-ttu-id="541e7-159">Découpage dans l’espace d’affichage</span><span class="sxs-lookup"><span data-stu-id="541e7-159">Clipping in view space</span></span>

<span data-ttu-id="541e7-160">Voici notre vertex dans l’espace d’affichage :</span><span class="sxs-lookup"><span data-stu-id="541e7-160">Here is our vertex in view space:</span></span>

![vertex dans l’espace d’affichage](images/vertex-clip.png)

<span data-ttu-id="541e7-162">Voici notre plan de découpage dans l’espace d’affichage :</span><span class="sxs-lookup"><span data-stu-id="541e7-162">Here is our clip plane in view space:</span></span>

![plan de découpage dans l’espace d’affichage](images/clip-plane-view.png)

<span data-ttu-id="541e7-164">Voici le produit scalaire du vertex et du plan de découpage dans l’espace d’affichage :</span><span class="sxs-lookup"><span data-stu-id="541e7-164">Here is the dot product of vertex and clip plane in view space:</span></span>

<span data-ttu-id="541e7-165">ClipDistance = **v** · **C**  =  *v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>o</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  <sub></sub> c</span><span class="sxs-lookup"><span data-stu-id="541e7-165">ClipDistance = **v** · **C** = *v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub> + *v*<sub>z</sub>*C*<sub>z</sub> + *C*<sub>w</sub></span></span>

<span data-ttu-id="541e7-166">Cette opération mathématique fonctionne pour un objet Direct3D 10 ou version ultérieure, mais ne fonctionne pas pour un objet Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="541e7-166">This math operation works for a Direct3D 10 or later object but won't work for a Direct3D 9 object.</span></span> <span data-ttu-id="541e7-167">Pour Direct3D 9, nous devons tout d’abord passer par notre transformation de projection dans l’espace.</span><span class="sxs-lookup"><span data-stu-id="541e7-167">For Direct3D 9, we must first get through our projection transform into clip space.</span></span>

### <a name="projection-matrix"></a><span data-ttu-id="541e7-168">Matrice de projection</span><span class="sxs-lookup"><span data-stu-id="541e7-168">Projection matrix</span></span>

<span data-ttu-id="541e7-169">Une matrice de projection transforme un sommet de l’espace d’affichage (où l’origine est l’œil de la visionneuse, + x est à droite, + y est haut et + z est en avance) dans l’espace.</span><span class="sxs-lookup"><span data-stu-id="541e7-169">A projection matrix transforms a vertex from view space (where the origin is the viewer's eye, +x is to the right, +y is up, and +z is straight ahead) into clip space.</span></span> <span data-ttu-id="541e7-170">La matrice de projection lit le vertex pour la capture de matériel et l' [étape de pixellisation](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage).</span><span class="sxs-lookup"><span data-stu-id="541e7-170">The projection matrix readies the vertex for hardware clipping and the [rasterization stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage).</span></span> <span data-ttu-id="541e7-171">Voici une matrice de perspective standard (les autres projections requièrent des maths différentes) :</span><span class="sxs-lookup"><span data-stu-id="541e7-171">Here is a standard perspective matrix (other projections require different math):</span></span>

<dl> <span data-ttu-id="541e7-172">taux *r*   de largeur/hauteur de fenêtre</span><span class="sxs-lookup"><span data-stu-id="541e7-172">*r*  ratio of window width/height</span></span>  
<span data-ttu-id="541e7-173">angle de visualisation de *α*  </span><span class="sxs-lookup"><span data-stu-id="541e7-173">*α*  viewing angle</span></span>  
<span data-ttu-id="541e7-174">distance *f*   de la visionneuse au plan lointain</span><span class="sxs-lookup"><span data-stu-id="541e7-174">*f*  distance from the viewer to the far plane</span></span>  
<span data-ttu-id="541e7-175">distance *n*   entre la visionneuse et le plan proche</span><span class="sxs-lookup"><span data-stu-id="541e7-175">*n*  distance from the viewer to the near plane</span></span>
</dl><span data-ttu-id="541e7-176">![matrice de projection](images/projection-matrix.png)</span><span class="sxs-lookup"><span data-stu-id="541e7-176">![projection matrix](images/projection-matrix.png)</span></span>

<span data-ttu-id="541e7-177">La matrice suivante est une version simplifiée de la matrice précédente.</span><span class="sxs-lookup"><span data-stu-id="541e7-177">The next matrix is a simplified version of the previous matrix.</span></span> <span data-ttu-id="541e7-178">Nous affichons la matrice de manière simplifiée afin de pouvoir l’utiliser ultérieurement dans l’opération de multiplication de matrice.</span><span class="sxs-lookup"><span data-stu-id="541e7-178">We show the matrix simplified so we can use it later in the matrix multiply operation.</span></span>

![matrice de projection simplifiée](images/projection-matrix2.png)

<span data-ttu-id="541e7-180">Nous transformons maintenant notre sommet d’espace d’affichage en espace de clip avec une matrice multiplier :</span><span class="sxs-lookup"><span data-stu-id="541e7-180">Now we transform our view space vertex into clip space with a matrix multiply:</span></span>

![multiplication de matrice](images/matrix-multiply.png)

<span data-ttu-id="541e7-182">Dans notre opération de multiplication de matrice, nos composants x et y sont légèrement ajustés, mais nos composants z et w sont très déformés.</span><span class="sxs-lookup"><span data-stu-id="541e7-182">In our matrix multiply operation, our x and y components are only slightly adjusted, but our z and w components are quite mangled.</span></span> <span data-ttu-id="541e7-183">Notre plan de découpage ne nous donnera plus ce que nous voulons.</span><span class="sxs-lookup"><span data-stu-id="541e7-183">Our clip plane won't give us what we want any more.</span></span>

### <a name="clip-space-clip-plane"></a><span data-ttu-id="541e7-184">Plan de découpage de l’espace</span><span class="sxs-lookup"><span data-stu-id="541e7-184">Clip space clip plane</span></span>

<span data-ttu-id="541e7-185">Ici, nous voulons créer un plan de clip d’espace disque dont le produit scalaire avec le sommet de l’espace disque nous donne la même valeur que **v · C** dans la section [découpage dans l’espace d’affichage](#clipping-in-view-space) .</span><span class="sxs-lookup"><span data-stu-id="541e7-185">Here we want to create a clip space clip plane whose dot product with our clip space vertex gives us the same value as **v · C** in the [Clipping in view space](#clipping-in-view-space) section.</span></span>

![plan de découpage](images/clip-space-clip-plane.png)

<span data-ttu-id="541e7-187">**v** · **C**  =  **v P** · **C**<sub>P</sub></span><span class="sxs-lookup"><span data-stu-id="541e7-187">**v** · **C** = **v P** · **C**<sub>P</sub></span></span>

<span data-ttu-id="541e7-188">*v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>o</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub>  =  *v* ₓ *P* ₓ *c*<sub>p ₓ</sub>  + *v*<sub>y</sub>*p*<sub>y</sub>*c*<sub>p <sub>y</sub></sub>  +  *v*<sub>z</sub>*A*<sub>y</sub>*c*<sub>p <sub>z</sub></sub>  +  *BC*<sub>P <sub>z</sub></sub>  +  *v*<sub>z</sub>*c*<sub>p <sub></sub></sub></span><span class="sxs-lookup"><span data-stu-id="541e7-188">*v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub> + *v*<sub>z</sub>*C*<sub>z</sub> + *C*<sub>w</sub> = *v* ₓ *P* ₓ *C*<sub>Pₓ</sub> +*v*<sub>y</sub>*P*<sub>y</sub>*C*<sub>P <sub>y</sub></sub> + *v*<sub>z</sub>*A*<sub>y</sub>*C*<sub>P <sub>z</sub></sub> + *BC*<sub>P <sub>z</sub></sub> + *v*<sub>z</sub>*C*<sub>P<sub>w</sub></sub></span></span>

<span data-ttu-id="541e7-189">À présent, nous pouvons diviser l’opération mathématique précédente par le composant vertex en quatre équations distinctes :</span><span class="sxs-lookup"><span data-stu-id="541e7-189">Now we can break the preceding math operation up by vertex component into four separate equations:</span></span>

![composant de vertex x du produit de plan de découpage](images/clip-space-clip-plane-equ1.png)

![composant du vertex y du produit de plan de découpage](images/clip-space-clip-plane-equ2.png)

![composant de vertex w du produit de plan de découpage](images/clip-space-clip-plane-equ3.png)

![composant de sommet z du produit de plan de découpage](images/clip-space-clip-plane-equ4.png)

<span data-ttu-id="541e7-194">Notre plan de découpage d’espace de vue et notre matrice de projection dérivent et nous donnent notre plan de clip d’espace.</span><span class="sxs-lookup"><span data-stu-id="541e7-194">Our view space clip plane and our projection matrix derive and give us our clip space clip plane.</span></span>

![plan de découpage de l’espace](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a><span data-ttu-id="541e7-196">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="541e7-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="541e7-197">Guide de programmation pour HLSL</span><span class="sxs-lookup"><span data-stu-id="541e7-197">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[<span data-ttu-id="541e7-198">Syntaxe de la déclaration des fonctions</span><span class="sxs-lookup"><span data-stu-id="541e7-198">Function Declaration Syntax</span></span>](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 